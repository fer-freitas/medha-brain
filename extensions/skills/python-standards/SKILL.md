---
name: python-standards
description: Padrões Python da empresa — estrutura, tipagem, lint, logging e erros. Use ao escrever ou revisar código Python.
---
# Padrões Python
- Python 3.12+; layout `src/`; `pyproject.toml`; dependências gerenciadas com `uv`.
- Tipagem completa (mypy estrito); `ruff` para lint e formatação.
- Nomenclatura PEP 8: `snake_case` funções/variáveis, `PascalCase` classes, `UPPER_CASE` constantes.
- Funções pequenas e puras no domínio; I/O nas bordas (adaptadores).
- Erros: exceções específicas; não use `except Exception` sem relançar ou registrar.
- Logging estruturado; nunca logue segredos ou dados pessoais.
- Datas com timezone (`datetime.now(UTC)`); dinheiro com `Decimal`.
