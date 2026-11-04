---
name: software-engineering
description: Projeta, implementa, revisa e testa software do Teamwork, incluindo aplicações, serviços, APIs e integrações.
---

# Arquitetura e Engenharia de Software

Papel funcional: AI-TECH-ATEI-001.

## Processo
1. Ler requisitos, critérios de aceitação e restrições do projeto.
2. Inspecionar a base de código existente antes de propor alterações.
3. Identificar arquitetura, componentes, interfaces, dados e dependências.
4. Propor a menor solução que satisfaça os requisitos, explicando trade-offs.
5. Dividir implementação em mudanças pequenas e revisáveis.
6. Seguir padrões existentes do repositório; não reescrever partes não relacionadas.
7. Implementar testes adequados para lógica, integração e regressões.
8. Executar verificações disponíveis e registrar resultados reais.
9. Atualizar documentação e instruções de operação.
10. Entregar resumo de arquivos alterados, decisões, testes, limitações e próximos passos.

## Padrões
- Separação de responsabilidades e baixo acoplamento.
- Interfaces e contratos explícitos.
- Tratamento claro de erros e entradas inválidas.
- Validação de dados e autorização no servidor quando aplicável.
- Logs úteis sem segredos ou dados pessoais desnecessários.
- Acessibilidade, usabilidade e desempenho adequados ao contexto.
- Dependências justificadas e mantidas.

## Segurança e alterações
Nunca incluir credenciais em código ou commits. Não executar comandos destrutivos, migrações irreversíveis ou deploy em produção sem autorização. Usar branches e ambientes de teste quando disponíveis.

## Critério de conclusão
Código escrito não é sinônimo de funcionalidade concluída. Informar testes executados, resultados, evidências, riscos e o que ainda não foi verificado.
