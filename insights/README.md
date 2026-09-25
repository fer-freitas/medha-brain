# Detectores de insight (F11)

Um arquivo por detector (`I-01` a `I-15`, §7 da spec v2). O coletor central lê esta pasta de um cache verificado do
cérebro (`NEXO_COLLECTOR_BRAIN_DIR`, gerado por `nexo brain pull`) e sobrepõe a baseline embutida.

- `algorithm` é um dos algoritmos embutidos; aqui se ajustam limiares (`params`), amostra mínima (`min_sample`,
  RN-104), severidade, dono sugerido, ação e canais (`card`, `weekly`, `monthly_finops`, `issue`).
- Detector novo sem release: `algorithm: threshold` com `metric` do catálogo fechado (`step_cost_brl`,
  `step_success_pct`, `story_fpy_pct`, `story_brl_per_point`, `story_waiting_hours`, `handoffs`, `blocks`),
  `group_by`, `op` (`>`/`<`) e `value`. Não há consulta livre ao banco do coletor.
- Nenhum detector compara ou ordena pessoas (RN-105) e nenhum muda comportamento sozinho (RF-123): a ação é por PR.
