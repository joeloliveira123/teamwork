# Arquitetura do runtime de agentes Teamwork

## 1. Conceito
Um agente é uma identidade de execução composta por: ID, diretoria, especialidade, Skill, modelo configurado, ferramentas permitidas, escopo de memória, política de aprovação e histórico de execuções. A chamada à API do modelo fornece inferência; o runtime fornece o comportamento de agente, estado, ferramentas, governança e continuidade.

## 2. Componentes

### Agent Registry
Catálogo declarativo dos 30 ATEIs. Cada registro aponta para uma Skill existente e define permissões, ferramentas, diretoria e limites. Não se deve criar 30 processos de modelo permanentes: cada identidade é isolada logicamente e invocada sob demanda.

### Orchestrator
Recebe uma demanda, identifica o objetivo, seleciona o agente ou sequência de agentes, cria tarefas com IDs, acompanha estados, gerencia dependências, repassa resultados e solicita validação. Delegações devem carregar contexto mínimo necessário e critérios de aceite.

### Agent Runtime
Carrega a Skill e a política do agente, monta o contexto da tarefa, consulta memória autorizada, chama o modelo configurado, valida a resposta e grava execução, consumo, status e evidências. Um agente não pode ampliar suas próprias permissões.

### Memory
- Working memory: contexto temporário da execução.
- Episodic memory: tarefas, mensagens, decisões e resultados anteriores do agente.
- Organizational memory: políticas, documentos e conhecimento compartilhado aprovado.
- Project memory: artefatos e decisões vinculados a um projeto.

Cada memória deve registrar origem, proprietário, classificação, data, retenção e permissões. O agente só recupera conteúdo que seu papel pode acessar. Memória não é fonte de autoridade: políticas e aprovações prevalecem.

### Tool Gateway
Todas as ferramentas passam por um gateway central. Cada ferramenta declara schema de entrada, efeito, risco, permissões, timeout e se exige aprovação. O agente não recebe acesso livre ao sistema operacional, shell, rede, navegador, contas ou arquivos.

### Approval Service
Ações classificadas como críticas geram uma solicitação persistente de aprovação. A execução fica bloqueada até decisão do CEO ou aprovador formal. Aprovação deve estar vinculada à ação exata, parâmetros, custo, destino, validade e plano de reversão; mudança material invalida a aprovação.

### Audit and Observability
Registrar agente, tarefa, execução, modelo, timestamps, estado, ferramentas chamadas, aprovações, erros, custo quando disponível e referências das evidências. Nunca registrar API keys ou segredos.

## 3. Ciclo de tarefa
1. INTAKE: receber objetivo e solicitante.
2. TRIAGE: classificar risco, diretoria e especialidade.
3. PLAN: definir plano, agentes, dependências e critérios de aceite.
4. APPROVAL: bloquear ações que exigem aprovação.
5. EXECUTE: executar uma tarefa isolada por agente.
6. REVIEW: validar resultado e evidências.
7. HANDOFF: delegar ou consolidar resultado.
8. COMPLETE / BLOCKED / FAILED: fechar com motivo e trilha de auditoria.

## 4. Estados
Tarefa: QUEUED, RUNNING, WAITING_APPROVAL, NEEDS_INPUT, SUCCEEDED, FAILED, CANCELLED. Execução: CREATED, CONTEXT_READY, MODEL_RUNNING, TOOL_RUNNING, REVIEWING, FINISHED, ERROR.

## 5. Segurança
- Menor privilégio por padrão.
- Separação entre identidade do agente e credenciais do provedor.
- Segredos apenas em variáveis de ambiente ou cofre apropriado.
- Prompt injection e conteúdo externo são tratados como dados não confiáveis.
- Limites de tokens, custo, duração, tentativas e concorrência.
- Idempotência para operações que possam ser repetidas.
- Logs sem segredos e com retenção definida.
- Ações externas, financeiras, legais, destrutivas e produção exigem aprovação explícita.

## 6. Escalabilidade
No computador com 4 GB de RAM, iniciar com um worker e concorrência baixa (1–2 tarefas), usando inferência remota. SQLite atende ao protótipo local; PostgreSQL e fila dedicada podem ser adotados quando houver execução multiusuário ou implantação em servidor. As 30 identidades podem existir desde o início sem manter 30 modelos/processos ativos.

## 7. Critérios para declarar um agente operacional
- Registro válido e Skill encontrada.
- Chamada de modelo configurada e testada.
- Memória persistida e isolamento verificado.
- Ferramentas limitadas por allowlist.
- Política de aprovação aplicada no backend.
- Logs e evidências disponíveis.
- Testes de falha, timeout, repetição e prompt injection aprovados.