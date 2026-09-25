---
name: dotnet-standards
description: Padrões .NET da empresa — estrutura, nomenclatura, async, DI, logging e erros. Use ao escrever ou revisar código C#/.NET.
---
# Padrões .NET
- .NET LTS atual; `Nullable` e `ImplicitUsings` habilitados; avisos tratados como erro no CI.
- Nomenclatura: PascalCase para tipos/membros públicos, camelCase para locais/parâmetros, `_camelCase` para campos privados, sufixo `Async` em métodos assíncronos.
- Camadas: `Api` → `Application` → `Domain`; `Infrastructure` implementa portas do `Application`. `Domain` não referencia infraestrutura.
- Async de ponta a ponta; nunca `.Result`/`.Wait()`; propague `CancellationToken`.
- Injeção de dependência pelo container padrão; sem service locator.
- Erros: exceções de domínio específicas; na API, `ProblemDetails` (RFC 9457); não vaze stack trace.
- Logging estruturado (`ILogger<T>` com templates `{Campo}`); nunca logue segredos ou dados pessoais.
- Validação de entrada na borda (FluentValidation ou DataAnnotations).
- Valores monetários com `decimal`; datas em UTC (`DateTimeOffset`).
