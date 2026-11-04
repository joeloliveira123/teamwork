# Fluxo de Aprovações

## Exige aprovação explícita
- Despesa, compra, pagamento, contratação ou alteração de orçamento.
- Contrato, obrigação jurídica ou compromisso externo em nome do Teamwork.
- Publicação, deploy, alteração ou operação em produção.
- Comunicação externa relevante ou campanha pública.
- Exclusão irreversível, migração destrutiva ou mudança de retenção.
- Acesso novo/ampliado a dados pessoais, sensíveis, financeiros ou restritos.
- Mudança material de objetivo, escopo, prazo, custo, política ou risco.
- Aceitação de risco residual relevante.
- Ação que afete terceiros ou seja difícil de reverter.

## Fluxo
1. Responsável prepara solicitação com contexto e ação exata.
2. Diretor funcional revisa necessidade, escopo e alternativas.
3. PMO verifica impacto em projeto, prazo, custo, dependências e baseline.
4. SEC avalia segurança/privacidade/conformidade quando pertinente.
5. FIN analisa impacto financeiro quando pertinente.
6. CEO ou delegado humano formalmente autorizado decide.
7. Registrar decisão, condições, limites e validade.
8. Executar somente após aprovação e verificação das condições.

## Estados
NAO_APLICAVEL; PENDENTE; APROVADA; APROVADA_COM_CONDICOES; REJEITADA; EXPIRADA; REVOGADA.

## Registro mínimo
ID; solicitante; projeto/tarefa; ação; justificativa; benefício; alternativas; custo/fonte; impacto; riscos; dados/sistemas afetados; reversibilidade; rollback; validade; recomendação; decisão; aprovador; data.

## Regras
Silêncio não é autorização. Aprovação vale somente para ação, escopo, custo, ambiente e período descritos. Mudança material exige nova avaliação. Skills não aprovam por inferência. Em dúvida sobre alçada, pausar e escalar.
