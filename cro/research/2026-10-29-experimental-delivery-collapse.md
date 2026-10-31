# Incidente de entrega experimental — 29/10/2026

**Tipo:** diagnóstico operacional, não experimento CRO e não hipótese de alteração da landing. **Responsável pelo encaminhamento:** ibombonato / gestor autorizado da conta. **Estado:** causa não identificada pelas fontes consultadas; verificar no Ads Manager/Meta antes de atribuir a queda à landing. Nenhuma configuração Meta foi alterada.

## Evidência nova e reproduzível

Conta `974182265670621`, BRL, America/Sao_Paulo; experimental `120250764485030505`, controle `120250926395490505`. Último dia completo: **28/out**. Coleta principal consolidada às **12:02:31 UTC de 29/out**. MCP oficial inicializado, schemas/conta/campos verificados; totais de 1/3/7/14 dias conciliados exatamente com Graph GET diário. Nova leitura Graph de entrega, independente dos campos de ações, confirmou os números de 28/out. Não é o caso anterior de entrega zerada na resposta combinada com ações.

| Dia completo | Investimento exp. | Impressões exp. | Cliques link exp. | LPV exp. | Leads proxy exp. |
|---|---:|---:|---:|---:|---:|
| 27/out | R$ 172,39 | 40.042 | 873 | 740 | 268 |
| 28/out | R$ 2,80 | 591 | 16 | 16 | 4 |
| Variação | −98,38% | −98,52% | −98,17% | −97,84% | −98,51% |

R$ 2,80 representam **1,87%** do orçamento diário nominal de R$ 150. Orçamento é referência de entrega média, não garantia de gasto diário; este valor, acompanhado pela queda de impressões/cliques, caracteriza uma anomalia de entrega a investigar, não evidência de alteração secreta do orçamento.

**Localização temporal:** breakdown horário da experimental em 28/out mostra 590 impressões, 16 cliques e R$ 2,80 entre **00:00–00:59 São Paulo**, mais uma impressão sem gasto reportado entre 11:00–11:59. A soma horária confere exatamente com gasto, impressões e cliques do dia; paginação esgotada. O controle teve 36.669 impressões, 855 cliques e R$ 153,85 distribuídos no dia, também conciliados por hora.

**Hoje é parcial:** nova consulta em torno de 09h03 São Paulo mostra R$ 9,89 / 1.352 impressões / 40 cliques na experimental. Existe alguma entrega em 29/out, mas isso **não comprova recuperação sustentada** nem deve ser misturado aos dias completos ou apresentado como nova CVR diária. O controle parcial tem R$ 18,99 / 3.987 impressões / 87 cliques.

## Bloqueios/configuração investigados em leitura

- Conta `account_status=1`, `disable_reason=0`, `spend_cap=0`: sem bloqueio global ou teto de anunciante indicado nesses campos. Isso **não exclui limites internos, billing ou restrições não expostas pela API**. O controle segue entregando na mesma conta.
- Campanhas ACTIVE, R$ 150/dia cada; experimental `updated_time` ainda 17/out, controle ainda 27/out. Estratégia `LOWEST_COST_WITHOUT_CAP`; nenhum novo bid cap identificado nos campos retornados. Não inventar valores para campos omitidos.
- Conjuntos ACTIVE; quatro anúncios experimentais ACTIVE, antigo PAUSED, controle ACTIVE. Nenhum `issues_info`/feedback de reprovação retornado. Não interpretar ausência de campo como auditoria completa de todos os estados internos.
- União dos IDs de anúncios/conjuntos igual à de ontem. Todos os campos dos ativos, copy, destinos, UTMs, tracking e atribuição reconferidos sem alteração; única diferença bruta no anúncio antigo PAUSED é a URL assinada da miniatura, mesmo criativo e demais campos.
- **MCP `ads_get_errors`: `[]`.** **`ads_insights_anomaly_signal`: nenhum sinal encontrado** para sobreposição, fadiga ou público estreito. Esses diagnósticos não cobrem todos os problemas de pacing/billing/restrição; não anulam a entrega real quase nula. MCP de atividades experimental também vazio.
- Graph GET de atividades da conta desde 21/out: **37 registros**, paginação esgotada, filtro incluindo campanhas, conjuntos e todos os anúncios descobertos; nenhuma nova edição relevante após a mudança já conhecida do controle em 27/out. Não há evidência de pausa/edição da experimental nessas fontes; ausência no log não estabelece a causa.
- Main/Pages `c8a16941814a43a040506a5330903587e5c16852`, build concluído em 26/out02:08:45Z. Ambas as landings HTTP 200 e HTML byte a byte igual ao commit. CRO-002 **não publicado**; CTA público ainda com cores anteriores. Nenhum novo commit de produção explica essa mudança de entrega.
- Script real do CTA executado em Node VM sem rede: dez casos comportamentais aprovados em produção/proposta; Lead antes da navegação normal, delay150ms preservado. Igualdade literal href/constante continua **FAIL** por query externa já documentada; não foi normalizada nem apontada como causa da entrega. Semântica WhatsApp não verificada. Zero eventos Meta reais ou entradas no grupo.

## O que os dados não demonstram

CVR experimental de **25% = 4/16**, IC95% Wilson **10,18%–49,50%**: amostra extremamente pequena, não evidência de deterioração da página. Lead é clique pré-navegação atribuído, não participante confirmado. Queda de impressões/cliques ocorre antes da landing; identificar essa perda não exclui todo problema posterior, mas impede atribuir o volume perdido à cor/copy do botão. Não há base para culpar Safari, declarar fadiga, erro de cobrança, penalidade ou pacing específico.

Novos anúncios somaram 9 LPV / 2 Leads / R$ 1,36, **56,25% de apenas 16 LPV**. A participação cresceu porque o denominador desabou; não representa validação dos criativos ou nova distribuição estável. Anúncio principal: 7 LPV / 2 Leads; texto4em1: zero LPV/Leads, com sete impressões. Contagens e gasto por anúncio/dispositivo/posicionamento conferem com o total; no breakdown de posicionamento do controle existe resíduo de R$ 0,000001, inferior a um centavo, sem discrepância nos totais principais.

## Controle: primeiro dia inteiro do orçamento de R$ 150

Mudança externa R$170→150 em27/out09:47:50SP permanece registrada;27/out é transição,28/out primeiro dia completo. Comparação descritiva com **médias diárias dos quatro dias completos 23–26/out**:

| Indicador do controle | 23–26/out | 28/out | Variação |
|---|---:|---:|---:|
| LPV/dia | 753 | 732 | −2,79% |
| Gasto/dia | R$ 166,98 | R$ 153,85 | −7,86% |
| CVR ponderada | 39,84% | 40,44% | +0,60 p.p. |
| CPL proxy | R$ 0,5566 | R$ 0,5198 | −6,62% |

Uma quarta-feira versus média de sexta–segunda, campanhas não randomizadas e mix diferente não permitem inferir efeito causal do orçamento/landing. Não comparar total de quatro dias com um único dia.

## Encaminhamento concreto e próximo gate

**ibombonato / gestor autorizado:** conferir o painel de veiculação e histórico da experimental/conjunto/anúncios no Ads Manager para **28/out a partir de 00h São Paulo**, alertas de revisão/restrição, limites efetivos e avisos de cobrança. Se não houver causa visível e a baixa entrega persistir, encaminhar ao suporte Meta com os IDs, dia e evidências acima. Não ativar/pausar, elevar orçamento, alterar público, trocar criativo ou rastreamento para tentar corrigir sem autorização. Esta é uma solicitação de investigação humana, não afirmação de que um chamado externo já foi aberto.

**Decisão CRO:** reutilizar somente PR #16; CRO-002 continua aguardando decisão humana. Não atribuir melhora/piora a um tratamento que ainda não está público, não reabrir CRO-001 e não iniciar outro experimento. Depois de publicação confirmada, cumprir baseline/plano pré-registrados e assinalar essa fase de subentrega; não excluir dias retroativamente para favorecer resultado. Projeções antigas de dias até volume deixam de ser confiáveis com 16LPV/dia e não serão extrapoladas.

**Próxima leitura prevista no job existente:**30/out09hSãoPaulo, incluindo29/out completo: reconsultar entrega/hierarquia/atividades e respostas humanas, verificar decisão/publicação#16 e então definir se a anomalia persistiu ou houve retomada. BL-01/BL-02 e o pedido de materiais de23/out permanecem registrados sem nova cobrança ou alteração de exposição.

**Artefatos:** `~/work/hermes-scratch/cro-icb-2026-10-29/`: `analysis.json`, `daily-graph.json`, respostas MCP, `traffic-audit.json`, `activities.json`, `delivery-probe.json`, `mcp-delivery-diagnostics.json`, `delivery-assessment.json`, `today-validation.json`, Pages/live, NodeVM e verificação remota. Diagnóstico e encaminhamento serão comunicados no relatório final automático; não houve envio direto, mutação Meta, merge/auto-merge/deploy ou alteração de HTML.
