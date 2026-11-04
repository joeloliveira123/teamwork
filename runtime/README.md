# Teamwork Runtime — camada de execução

Esta pasta especifica e inicia a implementação do runtime que transforma as Skills em agentes executáveis. As Skills são instruções; o runtime fornece identidade, execução isolada por tarefa, memória, ferramentas, permissões, fila e auditoria.

## Arquitetura inicial
- Python + FastAPI: API local para receber e consultar tarefas.
- SQLite: persistência local de agentes, tarefas, execuções, memória e aprovações.
- Provedor de LLM compatível com API HTTP: inferência remota configurável por variáveis de ambiente.
- Worker assíncrono: executa tarefas sem exigir 30 processos/modelos simultâneos.
- Skills em `.agents/skills/`: instruções especializadas carregadas conforme o agente.

## Recursos previstos
- 30 identidades de ATEIs independentes, cada uma com sua própria Skill e configuração.
- Execução por tarefa com contexto e histórico separados por agente.
- Memória de execução privada e memória organizacional compartilhada com controle de acesso.
- Ferramentas registradas em allowlist, com permissões por agente.
- Aprovações humanas persistidas e verificadas antes de ações críticas.
- Logs, rastreabilidade, tentativas, estados e evidências.

## Limites do primeiro MVP
O MVP começa com tarefas de texto e chamadas a um LLM remoto. Não executa comandos arbitrários, não movimenta dinheiro, não envia mensagens externas, não publica em produção e não acessa o navegador ou arquivos locais sem ferramentas explicitamente implementadas e autorizadas.

## Requisitos locais
Windows, Python 3.11 ou superior recomendado. O computador do usuário tem recursos limitados (4 GB de RAM), então a inferência será remota por API e o runtime local será leve. Não iniciar 30 modelos locais ou 30 workers concorrentes.

## Configuração
1. Copie `.env.example` para `.env`.
2. Configure o endpoint, o nome do modelo e a chave de API do provedor escolhido.
3. Instale dependências com `pip install -r requirements.txt`.
4. Inicie a API conforme as instruções do README principal do runtime.

Nunca faça commit do arquivo `.env` nem exponha chaves em logs, prompts ou GitHub.

## Estado
Fundação arquitetural documentada. A presença destes documentos não significa que a API, agentes, provedor ou integrações estejam ativos. A implementação deve ser testada localmente antes de ser considerada operacional.