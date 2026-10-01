---
name: iu-click
description: Como criar, ler e atualizar itens de trabalho no IU Click pelo MCP — hierarquia épico, feature, história e tarefa, campos obrigatórios, estados, tags e vínculos. Use sempre que for registrar ou consultar trabalho no IU Click.
---
# IU Click (tracker do Itaú)

O IU Click é a fonte oficial do trabalho. O Medha lê e escreve nele pelo MCP do IU Click (F19). Esta skill diz **como** preencher; o MCP faz a chamada.

> **A definir pela empresa (depende da documentação do MCP):** nomes exatos das ferramentas do MCP, dos campos e dos estados. Os nomes abaixo são o modelo esperado e devem ser ajustados quando o MCP estiver disponível.

## Hierarquia
```
Épico (objetivo de negócio, trimestre)
└── Feature (entrega de valor, algumas sprints)
    └── História (valor para o usuário, cabe na sprint)
        └── Tarefa (unidade técnica, um dia ou menos)
```
- Toda história pertence a uma feature; toda feature, a um épico.
- Bug aponta para a história ou a feature onde foi encontrado.

## Campos obrigatórios por tipo
| Campo | Épico | Feature | História | Tarefa |
|---|---|---|---|---|
| Título (verbo + resultado) | ✔ | ✔ | ✔ | ✔ |
| Descrição / narrativa | objetivo e métrica | problema, escopo, fora de escopo | "Como… quero… para…" | o que fazer e onde |
| Critérios de aceite | — | resumo | Gherkin completo | critérios técnicos |
| Critérios técnicos e de teste | — | — | ✔ (após refinamento técnico) | ✔ |
| Pontos / estimativa | — | — | ✔ | horas |
| Squad e responsável | ✔ | ✔ | ✔ | ✔ |
| Tags | produto | produto, release | stack, risco, `medha` | tipo |
| Links | — | spec, discovery | SDD, ADRs | PR |

## Estados e quem move
`Novo → Em discovery → Pronto para refinamento → Em refinamento técnico → Pronto (DoR) → Em desenvolvimento → Em revisão → Em homologação → Pronto para produção → Concluído`
- **Pronto (DoR)** só com o portão de Definition of Ready aprovado no Medha (`definition-of-ready`).
- **Concluído** só com o PR integrado, o deploy em produção e a GMUD fechada.

## Regras
- Crie a história no IU Click **depois** que o PM aprovar o pacote no Medha; o id do IU Click volta para o `backlog.yaml` (campo de vínculo externo) e para o nome da branch e do PR.
- Nunca duplique: busque pelo título e pela feature antes de criar.
- Atualize o estado pelo fluxo; não pule estados.
- Comentário no IU Click nunca leva dado pessoal, segredo ou trecho de log com dado de cliente.
- Tag `medha` em tudo que for executado pelo Medha (métrica de adoção).

## Checklist antes de gravar
- [ ] Item pai existe e está correto?
- [ ] Todos os campos obrigatórios do tipo preenchidos?
- [ ] Critérios de aceite em Gherkin (história)?
- [ ] Links para spec, SDD e ADRs?
- [ ] Squad, responsável e tags definidos?
