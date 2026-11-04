# Teamwork

O Teamwork é uma organização digital estruturada por diretorias, com responsabilidades especializadas, Skills reutilizáveis, governança humana e projetos rastreáveis.

## Como o repositório está organizado

A estrutura principal é dividida por **diretorias**. Cada diretoria terá seu próprio espaço, reunindo a visão geral da área, a função do diretor, os três ATEIs e suas respectivas Skills.

```text
teamwork/
├── diretorias/
│   ├── 01-inovacao-growth/
│   ├── 02-ia-tecnologia/
│   ├── 03-operacoes/
│   ├── 04-financeiro/
│   ├── 05-projetos-pmo/
│   ├── 06-marketing-vendas/
│   ├── 07-produto-design/
│   ├── 08-inteligencia-mercado/
│   ├── 09-dados-analytics/
│   └── 10-seguranca-compliance/
├── governanca/
├── protocolos/
├── projetos/
├── modelos/
├── testes/
├── AGENTS.md
└── README.md
```

> A árvore acima representa a estrutura-alvo. As diretorias serão organizadas e migradas gradualmente. Não considere uma pasta concluída até que seus arquivos tenham sido efetivamente criados e verificados.

## As dez diretorias

| Ordem | Diretoria | Código | Responsabilidade principal |
|---:|---|---|---|
| 01 | Inovação e Growth | INNO | Inovação, experimentação e crescimento |
| 02 | IA e Tecnologia | AI-TECH | Engenharia, IA, sistemas e infraestrutura |
| 03 | Operações | OPS | Processos, serviços, qualidade e continuidade |
| 04 | Financeiro | FIN | Planejamento, tesouraria e análise financeira |
| 05 | Projetos e Portfólio (PMO) | PMO | Planejamento, coordenação e controle de projetos |
| 06 | Marketing e Vendas | MKT | Marca, marketing, vendas e relacionamento |
| 07 | Produto e Design | PROD | Estratégia de produto, UX e design |
| 08 | Pesquisa e Inteligência de Mercado | MI | Mercado, concorrência e voz do cliente |
| 09 | Dados e Inteligência Analítica | DATA | Engenharia de dados, BI e ciência de dados |
| 10 | Segurança e Compliance | SEC | Segurança, privacidade, riscos e conformidade |

## Padrão interno de cada diretoria

Cada pasta de diretoria deverá conter:
- `README.md`: missão, escopo, responsabilidades, indicadores e interfaces.
- `diretor/`: identidade funcional, atribuições e Skill do diretor.
- `ateis/ATEI-001/`, `ATEI-002/`, `ATEI-003/`: perfil, responsabilidades, entregáveis e Skill de cada especialista.
- `processos/`: procedimentos próprios da diretoria, quando necessários.
- `documentos/`: políticas, referências e artefatos específicos da área, quando necessários.

## Governança e funcionamento

- O CEO humano é a autoridade máxima.
- O padrão de autonomia é **autonomia com aprovação**.
- Cada diretoria responde por sua especialidade e colabora com as demais.
- O PMO integra o portfólio e acompanha projetos, sem substituir os responsáveis técnicos.
- Ações financeiras, legais, externas, irreversíveis ou em produção exigem aprovação explícita.
- Nenhuma entrega é considerada concluída sem evidência verificável.

## Skills agora; agentes no futuro

Nesta fase, o Teamwork é uma estrutura documental e operacional baseada em Skills. As Skills definem como cada função deve trabalhar, mas não são agentes autônomos nem ficam executando tarefas em segundo plano.

APIs, modelos, memória técnica, ferramentas e execução autônoma poderão ser adicionados futuramente, sem alterar a organização fundamental por diretorias.

## Fases de trabalho

1. **PROJETAR:** compreender o objetivo, pesquisar e planejar.
2. **EXECUTAR:** produzir entregáveis dentro do escopo autorizado.
3. **GERENCIAR:** validar, acompanhar, controlar mudanças e registrar aprendizados.

## Estado da reorganização

A reorganização está sendo feita gradualmente, diretoria por diretoria. A estrutura-alvo e a ordem oficial estão definidas neste documento; cada diretoria será marcada como organizada somente após a migração e verificação de seus arquivos.
