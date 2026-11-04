# Diretorias do Teamwork

Este diretório é a entrada principal para a estrutura organizacional do Teamwork. Cada diretoria possui seu próprio espaço e reúne o diretor, seus três ATEIs, Skills e documentos especializados.

## Mapa organizacional

| Ordem | Diretoria | Código | Pasta |
|---:|---|---|---|
| 01 | Inovação e Growth | INNO | `01-inovacao-growth/` |
| 02 | IA e Tecnologia | AI-TECH | `02-ia-tecnologia/` |
| 03 | Operações | OPS | `03-operacoes/` |
| 04 | Financeiro | FIN | `04-financeiro/` |
| 05 | Projetos e Portfólio (PMO) | PMO | `05-projetos-pmo/` |
| 06 | Marketing e Vendas | MKT | `06-marketing-vendas/` |
| 07 | Produto e Design | PROD | `07-produto-design/` |
| 08 | Pesquisa e Inteligência de Mercado | MI | `08-inteligencia-mercado/` |
| 09 | Dados e Inteligência Analítica | DATA | `09-dados-analytics/` |
| 10 | Segurança e Compliance | SEC | `10-seguranca-compliance/` |

## Estado da organização

| Diretoria | Código | Estrutura principal |
|---|---|---|
| Inovação e Growth | INNO | Organizada; arquivos verificados na etapa anterior |
| IA e Tecnologia | AI-TECH | Organizada e conferida |
| Operações | OPS | Organizada e conferida |
| Financeiro | FIN | Organizada e conferida |
| Projetos e Portfólio | PMO | Organizada e conferida |
| Marketing e Vendas | MKT | Organizada e conferida |
| Produto e Design | PROD | Organizada e conferida |
| Pesquisa e Inteligência de Mercado | MI | Organizada e conferida |
| Dados e Inteligência Analítica | DATA | Organizada e conferida |
| Segurança e Compliance | SEC | Organizada e conferida |

O registro central em `runtime/agent-registry.yaml` aponta para as Skills canônicas em `diretorias/`. As Skills antigas permanecem preservadas durante a transição; não foram removidas.

## Padrão de conteúdo por diretoria

```text
nome-da-diretoria/
├── README.md
├── diretor/
│   └── SKILL.md
├── ateis/
│   ├── ATEI-001/
│   │   └── SKILL.md
│   ├── ATEI-002/
│   │   └── SKILL.md
│   └── ATEI-003/
│       └── SKILL.md
├── processos/
└── documentos/
```

As pastas opcionais `processos/` e `documentos/` serão criadas quando houver conteúdo real para elas. Não serão criadas pastas vazias apenas para preencher a árvore.

## Regra de migração

- Uma diretoria por vez.
- Preservar o conteúdo das Skills durante a migração.
- Atualizar referências e registros que apontem para os caminhos antigos.
- Verificar os arquivos novos antes de remover os antigos.
- Não declarar uma diretoria organizada até concluir a conferência.
