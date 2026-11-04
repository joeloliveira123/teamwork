# Teamwork — AI Enterprise Operating System

O Teamwork é o sistema operacional organizacional de uma empresa coordenada por agentes de IA, com governança humana, departamentos especializados, habilidades reutilizáveis e projetos rastreáveis.

## Objetivo
Centralizar neste repositório:
- Constituição, estrutura organizacional, autoridade e regras de aprovação.
- Skills compatíveis com Codex para orientar agentes em tarefas especializadas.
- Processos, protocolos, modelos, projetos, decisões e evidências.
- Testes para verificar se os agentes respeitam os procedimentos.

## Princípios
1. **CEO humano como autoridade máxima:** decisões estratégicas e compromissos relevantes permanecem sob controle humano.
2. **Autonomia com aprovação:** agentes podem pesquisar, analisar, planejar e executar atividades autorizadas; ações críticas aguardam aprovação.
3. **Evidência antes de conclusão:** nenhuma tarefa é considerada concluída sem artefato, teste ou evidência verificável.
4. **Especialização com coordenação:** departamentos executam seu trabalho técnico; o PMO integra e acompanha, sem substituir especialistas.
5. **Rastreabilidade:** projetos, tarefas, riscos, decisões, mudanças e aprovações recebem registros identificáveis.
6. **Segurança por padrão:** menor privilégio, proteção de segredos, revisão humana e ambientes de teste.

## Estrutura
- `AGENTS.md`: instruções gerais para o Codex neste repositório.
- `.agents/skills/`: skills especializadas. Cada pasta contém um `SKILL.md`.
- `governance/`: constituição, autoridade, aprovações e registros.
- `departments/`: dez diretorias organizacionais.
- `projects/`: portfólio e documentação de projetos.
- `protocols/`: comunicação, handoff e execução.
- `templates/`: modelos padronizados.
- `workflows/`: fluxos operacionais.
- `knowledge/`: métodos e referências internas.
- `tests/`: cenários de validação das regras.

## Departamentos
1. Inovação e Growth
2. IA e Tecnologia
3. Operações
4. Financeiro
5. Projetos e Portfólio (PMO)
6. Marketing e Vendas
7. Produto e Design
8. Pesquisa e Inteligência de Mercado
9. Dados e Inteligência Analítica
10. Segurança e Compliance

## Fases operacionais
- **PROJETAR:** entender o objetivo, pesquisar, definir escopo e planejar.
- **EXECUTAR:** distribuir tarefas, produzir entregáveis e integrar resultados.
- **GERENCIAR:** monitorar, validar, controlar mudanças e registrar aprendizados.

## Como usar com Codex
Abra/clique em **Open in Codex** ou clone este repositório e abra a pasta no Codex. O Codex deve ler `AGENTS.md` e consultar a skill pertinente em `.agents/skills/`. Skills são instruções reutilizáveis; elas não criam, por si só, agentes persistentes nem executam processos em segundo plano. Orquestração real entre agentes e memória operacional persistente exigirão ferramentas, integrações e infraestrutura adicionais.

## Estado atual
Fundação organizacional e primeira versão do PMO. As demais diretorias estão registradas como áreas planejadas; suas skills serão desenvolvidas e validadas progressivamente. Não interpretar diretórios planejados como agentes já implementados.

## Evolução
Mudanças de estrutura, permissões, políticas ou processos devem ser documentadas. Alterações críticas devem ser submetidas à aprovação do CEO.
