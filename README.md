# Teamwork

O Teamwork é uma organização digital estruturada por dez diretorias, com responsabilidades especializadas, Skills reutilizáveis, governança humana e projetos rastreáveis.

## Estrutura do repositório

```text
teamwork/
├── diretorias/       # 10 diretorias, diretores e 30 ATEIs
├── governanca/       # modelo operacional, autoridade e aprovações
├── protocolos/       # demandas, delegação, comunicação e mudanças
├── projetos/         # portfólio e registros de projetos
├── modelos/          # intake, tarefas, aprovações e relatórios
├── testes/           # testes de aceitação e qualidade
├── runtime/          # arquitetura futura; não ativada nesta fase
├── AGENTS.md
└── README.md
```

## As dez diretorias
| Ordem | Diretoria | Código |
|---:|---|---|
| 01 | Inovação e Growth | INNO |
| 02 | IA e Tecnologia | AI-TECH |
| 03 | Operações | OPS |
| 04 | Financeiro | FIN |
| 05 | Projetos e Portfólio (PMO) | PMO |
| 06 | Marketing e Vendas | MKT |
| 07 | Produto e Design | PROD |
| 08 | Pesquisa e Inteligência de Mercado | MI |
| 09 | Dados e Inteligência Analítica | DATA |
| 10 | Segurança e Compliance | SEC |

## Sistema Operacional
O fluxo padrão é: INTAKE → TRIAGEM → DESCOBERTA → PLANEJAMENTO → APROVAÇÃO (quando necessária) → EXECUÇÃO → VALIDAÇÃO → ACEITE → ENCERRAMENTO.

- O CEO humano é a autoridade máxima.
- Cada diretor funcional responde pela sua especialidade.
- Os ATEIs produzem entregáveis especializados.
- O PMO coordena projetos e dependências, sem substituir os responsáveis técnicos.
- Segurança e Compliance avalia riscos e controles.
- Gastos, contratos, ações externas, produção, exclusões irreversíveis e mudanças materiais exigem aprovação humana explícita.
- Nenhuma entrega é concluída sem evidência e aceite aplicável.

## Documentos principais
- [Índice das diretorias](diretorias/README.md)
- [Governança](governanca/README.md)
- [Protocolos](protocolos/README.md)
- [Modelos de trabalho](modelos/README.md)
- [Portfólio de projetos](projetos/README.md)

## Fase atual: Skills-first
Nesta fase, o Teamwork é uma estrutura documental e operacional baseada em Skills. As Skills definem como cada função trabalha; não são agentes autônomos e não ficam executando tarefas em segundo plano. APIs, memória técnica e execução autônoma poderão ser avaliadas futuramente, após maturidade dos processos.

O runtime é documentação/estrutura futura e não deve ser tratado como sistema operacional ativo.
