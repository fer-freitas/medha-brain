---
name: code-review-checklist
description: Checklist de revisão do Nexo focado em "o que foi pedido foi entregue". Use ao revisar histórias.
---
# Checklist de revisão
- Cada critério de aceite tem implementação **e** teste que o exercita de verdade.
- Casos de erro e limites cobertos; nenhum comportamento pedido ficou de fora; nada além do escopo.
- Contratos respeitados (rotas, payloads, códigos de status).
- Sem segredos, dados pessoais ou TODOs críticos; logs adequados.
- Mudança do tamanho certo; nomes claros; sem código morto.
- Se o problema é da especificação (ambígua/contraditória), marque `spec_issue`.
