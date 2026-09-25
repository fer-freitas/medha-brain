---
name: secure-coding
description: Codificação segura para negócio regulado — OWASP Top 10/ASVS, LGPD, segredos, logs sem PII. Use ao implementar ou revisar código.
---
# Codificação segura
- Valide toda entrada na borda (tipo, tamanho, formato); rejeite por padrão.
- Autorização em todo endpoint (negar por padrão); nunca confie em ids vindos do cliente sem checar propriedade.
- Consultas parametrizadas; nada de concatenar SQL/comandos.
- Segredos só via configuração segura/cofre; nunca no código, testes ou logs.
- Logs estruturados sem dados pessoais (mascarar CPF, e-mail, cartão); erros sem stack trace para o cliente.
- Criptografia: bibliotecas padrão da plataforma; TLS; hash de senha com algoritmo adaptativo.
- Dados pessoais: minimização, finalidade, retenção (LGPD).
