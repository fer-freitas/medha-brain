---
name: selo-low-risk
description: Critérios e evidências para uma mudança receber o selo low risk (aprovação simplificada da GMUD) — reversibilidade, testes, performance, segurança, tamanho e histórico. Use ao classificar o risco no refinamento e ao preparar a GMUD.
---
# Selo low risk

O selo permite aprovação simplificada da mudança. A candidatura é indicada no refinamento (`mudanca.candidata_low_risk`) e confirmada com as evidências da entrega.

> **A definir pela empresa:** critérios oficiais do selo e quem concede. A lista abaixo é a proposta de critérios verificáveis; o Medha confere os que são automáticos a partir do pacote de evidências.

## Critérios propostos
| Critério | Verificação | Automático |
|---|---|---|
| Reversível em minutos (alias, rollback, feature flag) sem perda de dados | plano de retorno + migração compatível | parcial |
| Sem mudança de contrato incompatível (API/evento) | teste de contrato | sim |
| Sem migração destrutiva de dados | análise da migração | parcial |
| Todos os critérios de aceite e técnicos com teste passando | rastreio AC/CT | sim |
| Cobertura das linhas alteradas ≥ mínimo | relatório | sim |
| Mutação ≥ mínimo | relatório | sim |
| Teste de carga dentro dos limites | relatório k6 | sim |
| Segurança sem achados bloqueantes | SAST/SCA/segredos/IaC | sim |
| Revisão independente aprovada | revisão do Medha + humana | sim |
| Tamanho da mudança limitado (ex.: ≤ 400 linhas, ≤ 1 serviço) | diff | sim |
| Serviço sem incidente causado por mudança nos últimos 30 dias | histórico (DORA/incidentes) | sim |
| Deploy com canário/rolling e rollback automático por alarme | configuração | parcial |

## Regras
- Qualquer critério não atendido → GMUD normal.
- Mudança em área de risco (pagamentos, dados pessoais, autenticação) só com selo se a empresa permitir.
- O pacote de evidências assinado acompanha a solicitação do selo.

## Checklist
- [ ] Candidatura indicada no refinamento
- [ ] Todos os critérios com evidência
- [ ] Pacote de evidências anexado
