---
name: gmud
description: Como preparar e abrir a GMUD (gestão de mudança) para produção — classificação de risco, janela, plano de implantação, plano de retorno, testes e evidências, comunicação e aprovadores. Use ao preparar uma entrega para produção.
---
# GMUD (gestão de mudança)

O Nexo monta o pacote de evidências assinado da entrega (`nexo evidence build`); a GMUD usa esse pacote como anexo e fonte das informações.

> **A definir pela empresa:** ferramenta da GMUD, campos oficiais, categorias de risco, janelas, antecedência mínima e aprovadores (CAB). Os campos abaixo são o modelo esperado.

## Conteúdo da GMUD
| Campo | De onde vem |
|---|---|
| Título e descrição da mudança | Histórias/feature (IU Click) |
| Justificativa de negócio | Discovery / feature |
| Serviços e componentes afetados | SDD + `nexo graph impact` |
| Classificação de risco | `mudanca.risco` do refinamento + critérios da empresa |
| Janela de implantação | Calendário da empresa, fora de congelamento |
| Plano de implantação (passo a passo) | Estratégia de deploy (`deploy-aws`) |
| Plano de retorno (rollback) e tempo estimado | `deploy.rollback` do refinamento |
| Testes realizados e resultados | Pacote de evidências: unitário, integração, contrato, carga, mutação, segurança |
| Validação pós-implantação | `validacao-pos-deploy` |
| Impacto em clientes e comunicação | PM |
| Responsáveis e contatos durante a janela | Squad |
| Selo low risk (se aplicável) | `selo-low-risk` |

## Regras
- GMUD só com a esteira verde até homologação e o teste de carga aprovado.
- Plano de retorno testado em homologação.
- Mudanças dependentes em sistemas diferentes: GMUDs relacionadas e ordem de implantação (`nexo program`).
- Após a janela: registrar resultado (sucesso, sucesso parcial, retorno) e evidências da validação pós-deploy.

## Checklist
- [ ] Todos os campos preenchidos a partir do pacote de evidências
- [ ] Plano de retorno com tempo estimado
- [ ] Janela fora de congelamento
- [ ] Aprovadores definidos
- [ ] Resultado registrado após a janela
