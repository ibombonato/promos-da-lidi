# Primeiro dia completo do clone e do targeting do controle — 2026-11-16

## Evidência nova e escopo
15/nov é o primeiro dia completo após a ativação externa do clone120252642171330505 e a edição de targeting do controle em14/nov. MCP oficial, Graph diário/horário e ad-day foram consultados hoje e conciliados exatamente. As duas campanhas originais continuam como endpoints separados; não somar clone ao experimental original ou interpretar LPV como pessoas únicas.

|Campanha / dia15/nov|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|
|Experimental original|R$155,49|20680|680|555|212|38,20%|R$0,73|
|Controle|R$145,04|20507|629|535|227|42,43%|R$0,64|
|Clone separado|R$57,13|7803|252|207|81|39,13%|R$0,71|

Clone: Wilson95% 32,74–45,92%. Contra o lançamento parcial14/nov (251LPV/84Leads=33,47%,R$83,06), CVR+5,66p.p.; **não comparar um total parcial com um completo como taxa de crescimento diário** ou declarar vitória com207LPV. Anúncio120252642196110505 concentrou206LPV/81Leads/R$56,43 (99,52%dosLPV),120252736506790505 teve1LPV/0Lead/R$0,70. Distribuição não é50/50;0/1 não demonstra inferioridade do segundo anúncio.

Readback de TODOS os anúncios/conjuntos/campanha do clone é idêntico ao de15/nov: campanhaACTIVE/R$50dia, dois adsACTIVE/umPAUSED; ambos ativos têm link explícito index3.html. Não depender do nome/UTM nem da permissão do post, cujo conteúdo não foi observado nesta execução. Pixel/eventos/atribuição preservados. O controle mantém targeting observado ontem (mobile;location_types frequently_in+home+recent), sem inferir que isso causou CVR42,43%. Campanhas originais seguemACTIVE/R$150dia.41atividades desde14/nov paginadas, nenhuma relevante após15/nov00h; quatro drafts idênticos àvéspera, não publicados/ativados pelo agente. Ativos originais/copy/URLs/tracking inalterados; única diferença bruta éminiatura assinada de um ad antigoPAUSED, mesmoIDcriativo/restantescampos.

## Entrega concreta / handoff
**ibombonato, gestor autorizado:** a nova exposição compartilhada agora possui um dia completo confirmado; tratar a leitura do clone como diagnóstico próprio. Avaliar sua alocação desigual no Ads Manager, não redistribuir nem ativar/desativar anúncios por este agente. Não é chamado de suporte aberto ou recomendação de mudança sem autorização. Gate real da otimização continua a decisão humana no[PR#16](https://github.com/ibombonato/promos-da-lidi/pull/16), não esperar outra janela arbitrária depois da rotação de convite.

## Refinamento objetivo do próximo plano BL-02 — sem implementar
Problema: a imagem/ornamento do topo ocupa espaço antes da oferta; protótipo já mediu CTA129px mais cedo em390/360, mas perda de confiança por foto menor não foi medida. Manter intervenção única: compactar somente módulo mobile, preservando copy/CTA/cores que vierem a ser aprovadas,tracking e rotas. ICEI8/C5/E8 não inflado por estes resultados.

**Novo guard de exposição pré-especificado:** após encerrar explicitamente CRO-002, preparar BL-02 com resultado principal exclusivo120250764485030505. Congelar pesos de anúncio/dispositivo a partir do pré-período pela regra escolhida antes do teste; registrar separadamente tráfego do clone e transição14/nov do controle, sem combinar taxas ou eliminar15/nov. Fazer sensibilidades por fase com durações inclusivas/LPVdia/gastodia; nenhuma compensação causal por somar marginais. Manter CVR primária/CPL secundária; não substituir endpoint pelo anúncio que recebeu quase todo gasto ou melhorou no dia. Amostra/checkpoint de BL-02 será calculado para seu próprio baseline, não herdado doCRO-002; gates restantes de zoom/texto ampliado preservados. A mudança de controle/clone é contexto, não tratamento da landing ou justificativa para aguardar indefinidamente.

Próxima observação17/nov09hSP:16/nov completo, segunda jornada completa dessas condições; checar decisão#16/PagesSHA+HTML, alocação do clone,mix originais e revisões. Sem nova cobrança dos materiais reais já pedidos23/out/comprovação20.000/estrelas03/nov. Nenhum IDnovo/segundoPR/alteraçãoMeta.

Fontes locais: clone-audit.json,mcp-clone-result.json,daily-graph.json,traffic-audit.json,expanded-activities.json,entity-changes.json,today-validation.json e daily-contribution.json em ~/work/hermes-scratch/cro-icb-2026-11-16/. Todas coletas atuais; anteriores somente para comparação identificada.
