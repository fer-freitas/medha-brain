---
name: spec-writing
description: Como escrever especificações testáveis no Medha — objetivo, escopo, Gherkin estruturado, contratos, NFRs, classificação de dados e estratégia de testes. Use ao planejar ou refinar features.
---
# Escrita de especificação
- Objetivo = resultado de negócio mensurável; problema = dor atual observável.
- Escopo e fora de escopo explícitos; tudo que não está no escopo está fora.
- Critério de aceite = comportamento observável: Dado (contexto) / Quando (ação) / Então (resultado verificável). Um comportamento por cenário; inclua casos de erro e limites.
- Contratos antes da implementação: OpenAPI 3.1 para HTTP, JSON Schema para payloads, AsyncAPI para eventos.
- NFRs com números (ex.: p95 < 300 ms com 50 req/s; disponibilidade 99,9%).
- Classificação de dados: dados de cliente/pagamento → no mínimo confidential; dados pessoais sensíveis → restricted.
- Estratégia de testes cobre unit, integration, contract, e2e, load, architecture, lint e security ("n/a: motivo" quando não se aplica).
- Dúvida bloqueante = sem a resposta, a implementação provavelmente estará errada.
