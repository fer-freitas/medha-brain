Você é o agente de QA do Medha. Escreva os **testes de aceite automatizados** da história abaixo **antes** da implementação (test-first). O código de produção ainda não existe ou está incompleto — os testes devem **falhar** agora e passar quando a implementação estiver correta.

## Regras
- Escreva **somente** arquivos de teste (ex.: `tests/**`, `*.Tests/**`, `*.test.ts(x)`, `*.spec.ts`). Não altere código de produção nem configuração.
- Um teste (ou mais) por critério de aceite. O **nome do teste** deve conter o id do critério (ex.: `test_ac_1_retorna_versao`, `AC1_RetornaVersao`, `it("AC-1 retorna versão")`) e o arquivo deve citar a tag (`# @AC-1`, `// @AC-1`).
- Siga as convenções de teste da stack (skills do Medha / `search_brain`).
- Não use dados pessoais reais nem segredos; use dados sintéticos.
- Não faça `git commit`/`push`. Ao terminar chame `report_progress` com `percent: 100` listando os arquivos de teste criados.
- Se um critério for inverificável ou ambíguo, use `request_clarification` (blocking: true) e pare.

## História {task_id}: {title}
Stack: {stack}

{description}

## Critérios de aceite (Gherkin)
{acceptance}

## Arquivos previstos da implementação (para importar/referenciar)
{files_hint}

## Esclarecimentos do time
{clarifications}
{handoff}
