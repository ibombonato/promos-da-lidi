# BL-02 — Preparação com sensibilidade ao mix de anúncios

**Data:** 27/10/2026. **Estado:** refinamento documental, não implementado; não é CRO-003. CRO-002 continua Em PR #16, não publicado. Não altera seu endpoint, baseline ou referência de planejamento4170LPV. Complementa a especificação da primeira dobra de24/out; não cria tratamento concorrente.

## Evidência nova: não presumir que o mix permanece irrelevante

Coleta atual MCP oficial + Graph GET, dias completos America/Sao_Paulo, totais conciliados. Mesmos quatro anúncios experimentais ativos, configurações/copy/UTMs/atribuição inalteradas; a distribuição efetiva mudou, sem nova edição identificada. Os dois anúncios lançados no fim de21/out passaram de34/789LPV (4,31%) em25/out para105/597 (17,59%) em26/out. Os volumes continuam pequenos para julgar sua qualidade, mas já não é correto repetir que têm somente15LPV ou participação residual constante.

| Anúncio experimental | 25/out Leads/LPV | CVR | Share LPV | 26/out Leads/LPV | CVR | Share LPV |
|---|---:|---:|---:|---:|---:|---:|
| Texto4em1 `120250848857170505` | 19/67 | 28,36% | 8,49% | 12/42 | 28,57% | 7,04% |
| Produtos atualizados `120251541120490505` | 251/688 | 36,48% | 87,20% | 194/450 | 43,11% | 75,38% |
| Novo `120252297350870505` | 9/21 | 42,86% | 2,66% | 27/84 | 32,14% | 14,07% |
| Novo `120252297350880505` | 5/13 | 38,46% | 1,65% | 9/21 | 42,86% | 3,52% |

CVR agregada experimental35,99%→40,54%, mudança+4,54p.p. Decomposição simétrica verificável, com w=shareLPV e p=Lead/LPV:

- Parcela aritmética de composição: soma[(w26−w25)×(p26+p25)/2] = **−0,08p.p.**
- Parcela aritmética dentro dos anúncios: soma[(p26−p25)×(w26+w25)/2] = **+4,62p.p.**
- Soma=+4,54p.p.; identidade reconciliada sem arredondamento antes da soma.

**Interpretação limitada:** o crescimento dos novos anúncios não explica aritmeticamente a recuperação diária como um simples efeito positivo de composição. Isso não isola qualidade de tráfego dentro do anúncio, leilão, dia da semana, atribuição ou aleatoriedade; as parcelas não são efeitos causais. Não há novo tratamento de landing publicado, portanto não atribuir a recuperação ao contraste, à arquitetura futura ou a uma vitória tardia do CRO-001. Não concluir que a distribuição futura será neutra porque a parcela de mix de um único par de dias ficou próxima de zero.

## Hipótese futura delimitada e priorização

**Problema hipotético:** a auditoria real de24/out mostrou hero248px/foto128px antes da oferta, CTA já visível e grade de benefícios parcialmente abaixo da dobra. Não foi medido abandono por essa causa.

**Mudança objetiva futura:** compactar exclusivamente o módulo mobile da marca/foto para os alvos previamente especificados (hero136px, foto88px, padding superior do conteúdo34px); preservar literalmente oferta/headline, CTA/cor então aprovada, argumentos, recursos, destinos e scripts. Tratar o módulo como uma intervenção, não como isolamento de cada propriedade CSS. Não simplificar simultaneamente o rótuloBL-06 nem adicionar ofertas/prova social.

**Justificativa/comportamento esperado:** antecipar reconhecimento da oferta e dos benefícios em diferentes entradas de anúncio, sem depender de promessas ou imagens ainda não comprovadas. O aumento observado do tráfego de novos anúncios reforça a necessidade de medir consistência por origem; não aumenta a confiança de que o hero cause abandono.

**ICE mantido:** I8/C5/E8, avaliação qualitativa, não lift previsto. BL-01 continua prioritário se houver material real autorizado; BL-02 é alternativa sem esse material. Pedido23/out continua pendente, sem nova cobrança. Nenhum novo ID CRO, HTML ou exposição alterado.

## Plano operacional adicional para o futuro teste, não mudança no CRO-002

1. Após avaliar/encerrar CRO-002 e confirmar ausência de PR experimental pendente, revalidar a prioridade. Usar somente a versão imediatamente anterior como baseline do futuro teste; nunca misturar tratamentos para aumentar amostra.
2. **Primária:** Lead/LPV agregado, CPL secundário, conforme plano da hipótese. Escolher baseline/MDE/checkpoint de volume e cobertura semanal antes de observar o pós; não substituir a métrica principal por um segmento favorável. Publicação exige PagesSHA+HTML; excluir dia misto. Não reciclar4170/4128 como limite universal.
3. **Sensibilidade previamente definida:** congelar IDs e shares de LPV por anúncio do pré-período escolhido, antes de ler o pós. Exibir contagens, CVR e shares antes/depois; acrescentar CVR padronizada pelos shares congelados. Comparar controle pela sua própria composição, sem fingir que anúncios distintos são o mesmo estrato.
4. Se surgir anúncio novo sem baseline, mostrar sua contribuição separada e cobertura percentual dos anúncios comuns. Na sensibilidade dos comuns, explicitar renormalização dos pesos e que a estimativa é condicional; não imputar taxa prévia, somar aliases, interpretar null como zero, nem reponderar a primária. Anúncio antigo sem LPV pós impede sua taxa padronizada: declarar não estimável nessa cobertura, sem preencher silenciosamente.
5. Mostrar análise por dispositivo/posicionamento como contexto, sem selecionar resultados ou diagnosticar Safari por um gap. Datas e revisões preservadas; pequenas células não recebem conclusão de superioridade. Intervalos binomiais descritivos não corrigem dependência, atribuição ou falta de randomização.
6. Avaliação principal no checkpoint previamente registrado; se agregado e sensibilidades forem inconsistentes ou incertos, registrar Inconclusivo com limites, sem esperar indefinidamente por significância. A decomposição diária acima é diagnóstico de preparação, não teste de eficácia, critério de parada ou mudança do endpointCRO-002.

**Fontes reproduzíveis:** snapshot27/out em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-27/`: `daily-evidence.json`, `analysis.json`, `traffic-audit.json`, `additional-validation.json`, respostasMCP atuais; referência25/out reconsultada no diário atual e métricas por anúncio no snapshot26/out preservado. O uso do snapshot anterior na decomposição é explicitamente comparativo, nunca substituto de coleta atual. Nenhuma mutação Meta ou nova landing implementada.
