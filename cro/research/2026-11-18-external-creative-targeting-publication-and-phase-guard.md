# Meta CRO — verificação somente leitura em 18/11/2026

Conta 974182265670621, BRL, America/Sao_Paulo; dias completos até 17/11. MCP oficial negociado 2025-11-25; somente ferramentas de leitura e Graph GET. Nenhuma edição no repositório/Meta.

## Totais exatos MCP × Graph

| Janela | Campanha | Gasto R$ | Impressões | Cliques | LPV | Leads proxy | CVR | CPL R$ |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-17–2026-11-17 (1d) | experimental | 144.12 | 22279 | 688 | 574 | 190 | 33.10% | 0.7585 |
| 2026-11-17–2026-11-17 (1d) | controle | 151.39 | 20670 | 596 | 495 | 160 | 32.32% | 0.9462 |
| 2026-11-15–2026-11-17 (3d) | experimental | 482.78 | 72474 | 2245 | 1844 | 646 | 35.03% | 0.7473 |
| 2026-11-15–2026-11-17 (3d) | controle | 476.41 | 67577 | 1918 | 1611 | 627 | 38.92% | 0.7598 |
| 2026-11-11–2026-11-17 (7d) | experimental | 1071.34 | 154466 | 4968 | 4036 | 1410 | 34.94% | 0.7598 |
| 2026-11-11–2026-11-17 (7d) | controle | 1069.46 | 163042 | 4350 | 3660 | 1373 | 37.51% | 0.7789 |
| 2026-11-04–2026-11-17 (14d) | experimental | 2083.91 | 315013 | 10083 | 8307 | 2929 | 35.26% | 0.7115 |
| 2026-11-04–2026-11-17 (14d) | controle | 2089.68 | 373713 | 9431 | 7936 | 2944 | 37.10% | 0.7098 |

## Nova exposição externa verificada

- Original: público alterado em 17/11 às 18:43:10 SP, 24–50 → 22–45 e mobile → mobile+desktop. Criativos trocados nos anúncios 120251541120490505 (2214895639068786 → 1161944266575059) e 120252297350870505 (1319677443530855 → 2282920992488231). No primeiro, 2 → 7 corpos de texto ativos; as cinco sugestões anteriores estão agora no asset_feed_spec vivo. Destino/código UTM nos campos de criativo preservados. Demais mudanças de timestamp/revisão não foram confundidas com criativo.
- Drafts atuais: 0, antes 4. A constatação de alteração vem do Graph e log de atividades, não apenas do desaparecimento dos drafts.
- Clone: novo conjunto 120252802517710505, Advantage+ Audience=1 e faixa configurada 22–65, difere do original 120252642175430505, Advantage+=0 e 22–50. Três novos anúncios configurados (dois ativos e um pausado). Primeira entrega do anúncio 120252802517820505 às 18:55:59 SP de 17/11; o 120252802517800505 começa em 18/11 às 02:32:18 SP. Compartilham orçamento da campanha, não são um teste aleatorizado.

## Primeiro dia completo após interesse O Boticário — separar conjuntos

| Data / conjunto | Gasto R$ | LPV | Leads proxy | CVR | CPL R$ |
|---|---:|---:|---:|---:|---:|
| 2026-11-15 / original do clone | 57.20 | 207 | 81 | 39.13% | 0.7062 |
| 2026-11-16 / original do clone | 58.54 | 211 | 66 | 31.28% | 0.8870 |
| 2026-11-17 / original do clone | 42.63 | 178 | 71 | 39.89% | 0.6004 |
| 2026-11-17 / novo, parcial | 2.05 | 0 | 0 | n/a | n/a |

17/11 é o primeiro dia completo após a edição de interesse de 16/11 13:51:21 SP no conjunto original do clone. Diferença CVR original 17 vs 15: +0.76 pp (IC95% descritivo -9.04 a 10.55 pp). Volume de um dia não estabelece ganho. O total da campanha em 17/11 (178 LPV/71 Leads, R$44,68) mistura o conjunto novo no fim do dia; não atribuir o resultado ao interesse.

## Verificação e ressalvas

- PASS dos totais primários: 1/3/7/14 dias e baseline históricos batem MCP × Graph em gasto exato, impressões, cliques, LPV e Leads. Todas as datas diárias presentes; ad-day/adset-day e horas reconciliam. ALERTA: clone por dispositivo/posição soma R$44,67 contra R$44,68 nos totais atuais; contagens exatas, residual -R$0,01 persistente após repetição e consulta delivery-only. Gate monetário desses breakdowns NÃO passou; nenhum valor foi imputado nem tolerância relaxada.
- Revisões vs coleta anterior: original em 16/11 +R$0,02/+1 impressão; controle +R$0,01/+1 impressão; clone +R$0,13/+21 impressões/+2 cliques, sem revisão de LPV/Lead. Preservados snapshots iniciais desta execução e respostas brutas.
- Alguns IDs exclusivos de atividade first_delivery não são consultáveis por Graph (code100/subcode33 inclusive id,name). Não foram tratados como anúncios acessíveis adicionais nem gasto oculto. O roster configurado e totais continuam conciliados.
- Lead é clique de intenção antes da navegação, não entrada confirmada. Seleção de aliases, sem somas. Atribuições de campanhas nunca agrupadas. Baseline36 sem denominador/data não recebe teste estatístico.
- CRO001 permanece Inconclusivo com endpoint 14–21/out; alterações externas não o reabrem. CRO002 continua dependente de publicação verificada pela rotina principal; métricas não demonstram publicação da PR16. Dia 17 é misto no original; a sensibilidade 10–16/11 é adicional e não substitui séries/endpoint. Não criar nova espera arbitrária nem resetar experimento.


## Handoff e entrega concreta para o próximo teste

**Responsável: ibombonato/gestor autorizado.** Confrontar no Ads Manager as publicações externas de17/nov18:43SP e a nova estrutura do clone. São mudanças de exposição confirmadas, não instrução para pausar, alterar ou desfazer Meta. Não atribuir a queda de CVR do dia à edição intradiária. IDs de atividade inacessíveis e diferença monetária de1centavo nos breakdowns do clone continuam ressalvas, não gasto oculto demonstrado.

**BL-02 refinado, não implementado:** manter compactação exclusivamente mobile do módulo da primeira dobra, sem trocar headline/copy/CTA/links/scripts, ICE qualitativo **I8/C5/E8**, confiança no lift não aumentada. Antes de eventual implementação, arquivar configuração de cada ID de anúncio/conjunto e sua versão de criativo; um anúncio com o mesmo ID pode passar a outro tratamento de copy. Sensibilidades por anúncio devem cruzar ID com fase de criativo, e novo conjunto do clone precisa série separada. Preservar primária Lead/LPV da campanha original e controle contextual, sem pooling/alegar coortes únicas. Dia17/nov misto não desaparece da série;18/nov será primeiro dia completo do novo público/copy original. Não escolher outro endpoint só pelo resultado, impor14dias extras de espera ou interromper a aprovação do contraste por rotina de convite.

**Plano CRO-002 preservado:** segue Em PR#16; gate é decisão humana e confirmaçãoPagesSHA+HTML. Ao publicar, congelar14dias completos anteriores e excluir dia parcialmente exposto; revalidar uma única vez a referência de planejamento4170LPV antes de examinar desfecho. As fases Meta/clone/alegação social são sensibilidades e limitações, não uma redefinição seletiva do baseline. Pedidos23/out de ofertas reais e03/nov de comprovação20.000/estrelas continuam pendentes, sem nova cobrança.

**Incerteza principal7d:** diferença experimental−controle -2,58p.p., IC95% nominal -4,73 a -0,43. Semanas04–10→11–17/nov: variação relativa experimental-1,77%, controle2,11%, diferença entre evoluções-3,88pontos percentuais. Eventos atribuídos/dependentes, campanhas distintas/múltiplasleituras/mix não permitem causalidade; nenhuma taxa mede o contraste não publicado.

**Fontes:** artefatos atuais scratch2026-11-18: analysis.json, diagnostic.json, phase-contribution.json, semantic-diff.json, active-ad-readback.json, rawsMCP/Graph e revisões preservadas. Totais1/3/7/14d exatos; não declarar conciliação monetária dos breakdowns do clone como aprovada. Helpers reutilizados como código, nunca métricas antigas.
