---
name: testing-dotnet
description: Convenções de testes .NET no Nexo — xUnit, nomes com id de critério, Testcontainers, NetArchTest. Use ao escrever testes C#.
---
# Testes .NET
- xUnit em projeto `<Projeto>.Tests`; métodos `AC1_<Comportamento>` para aceite, com comentário `// @AC-1`.
- FluentAssertions opcional; Arrange/Act/Assert; `[Fact]`/`[Theory]`.
- Integração: `WebApplicationFactory` para APIs, Testcontainers para banco.
- Arquitetura: NetArchTest (Domain não referencia Infrastructure).
- Cobertura via `XPlat Code Coverage` (coverlet).
