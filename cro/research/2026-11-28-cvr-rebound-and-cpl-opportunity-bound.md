# 28/nov — recuperação da CVR não equivale a recuperação do custo

## Entrega concreta: dimensão do problema e limite da hipótese de landing

CRO-002 continua **Em PR#16, não publicado**; CRO-001 permanece Inconclusivo e encerrado. Publicação atual `79133f0fdddbfc64cd1c84ac0465c41a27eadf70`, deployment8100580176 e Actions45930958360 success; ambos HTMLs públicos coincidem byte a byte com main. A proposta de contraste não recebeu exposição. Nenhum novo ID ou tratamento criado.

**Evidência nova:** 27nov experimental145/398=36,43%, controle255/647=39,41%; contra26nov, taxas subiram3,18/2,61p.p. Na fase26–27 versus20–24nov, porém, CPL aumentou31,13%/30,72%; não houve recuperação da eficiência. A comparação respeita médias civis, dois versus cinco dias, e mantém25nov misto após os aumentos externos de orçamento. Original150 permanece; controle300/clone150. Campanhas não randomizadas, duas datas pós-orçamento, efeitos de dia da semana e mix não isolados: não é prova de causa ou de canibalização.

### Limite quantitativo para não prometer uma solução cosmética

Original20–24nov: 1000/2706=36,95% e CPLR$0,71;26–27nov: 283/813=34,81% e CPLR$0,94. Identidade CPL=CPM/(1000×CTRlink×LPV/clique×Lead/LPV) verificada no relatório completo sem arredondar.

**Contrafactual puramente aritmético:** congelando os outros componentes observados26–27nov, igualar o CPL20–24 exigiria CVR45,64%, ou +10,83p.p. Um aumento hipotético de +3p.p. a partir dessa taxa resultaria em CPLR$0,86, ainda20,72% acima da referência. São contas condicionais, não efeito previsto do contraste/BL-02, nem novo alvo de sucesso. O orçamento não será alterado e não há autorização para tentar compensar o custo por ediçõesMeta.

**Aprendizado:** melhora modesta de landing pode ser útil sem compensar a pressão contemporânea do restante do funil; não rejeitar teste útil por não recuperar todoCPL e não chamar aumento/queda deCPL de lift deCVR. Preservar CVR primária e CPL secundária. A escala de contraste/compactação não deve ser vendida como recuperação garantida do custo anterior.

## Próxima hipótese preparada — BL-02, sem implementação

- **Problema:** o módulo superior mobile ocupa cerca248px, enquanto oferta/CTA aparecem mais abaixo; protótipo anterior já demonstrou antecipação natural de129px. São evidências de geometria, não de compreensão ou conversão.
- **Proposta única:** compactar somente a arquitetura do módulo superior mobile, preservando copy, CTA, cores então aprovadas, scripts, Pixel, destinos e desktop baixo. Não adicionar prova social, ofertas, CSS deCTA nem nova rota.
- **ICE:** impacto8/confiança5/facilidade8, qualitativo; a conta deCPL dehoje não aumenta confiança emlift. Não atribuir IDCRO antes de implementar.
- **Refinamento de hoje:** aceitar CVR como critério de resultado mesmo quando CPL não recuperar a referência de leilão, e registrar lado a lado o contrafactualCPL limitado acima. Antes de publicar, calcular MDE e volume próprios da hipótese, com baseline congelado temporalmente e sem escolher a semana mais barata. Não reutilizar4170 como universal e não elevarMDE só para recuperar custo histórico.
- **Teste planejado:** somente após disposição/avaliação deCRO002;14dias completos anteriores por regra temporal, excluir dia misto depublicação, endpoint original agregado sem filtrar osads atualmenteativos; IC95%nominal e cobertura de diassemana, sensibilidade de fases14/17/19/23/25 e mixsem pooling doclone. Mesmo quando taxa sobe e custo piora, reportar ambos sem substituir endpoint. Gates técnicos: escopo exato + desktopbaixo + textoampliado + Chromium390/360 + NodeVMsemrede. Nenhum material opcional é bloqueio paraBL02.

## Gate real e handoff

**ibombonato: aprovar, pedir ajuste ou rejeitar#16.** Headpinado `ec21cb1a71bec5a45371faac9d1e3112b077af90`: integração prospectiva sem conflito, exatamente duas coresCSS, controle/copy/scripts/convites atuais preservados,0reviews e0checks/contextos/Actions dePR. `pending` com0contexts não é teste falhando. Não falta amostra deCRO001 nem material paraeste teste. Não fazer merge/auto-merge/deploy. As propostas operacionais antigas continuam separadas e não foram adotadas.

Após eventual publicação humana, confirmarPagesSHA+HTML, congelar14dias anteriores/excluir dia misto e revalidar uma vez referência4170 conformeplano deCRO002, sem trocar oendpoint em função doCPL favorável. Sem implantação paralela deBL02.

## Qualidade e execução

MCPoficial/schema/conta/campos/protocolo2025-11-25/mesmasessão;GraphGETpaginação e12células primárias exatas,36/36checks deste snapshot;302arquivos do manifesto reverificados pelo pai. Quatro divergências monetárias iniciais de-0,02 resolvidas por releituras atuais imutáveis; isso não comprova estabilidade futura nem altera as limitações deontem. Revisões26nov de mídia/impressões registradas, LPV/Lead inalterados. iPadcontrole1LPV/2Lead mantido comWilson indefinido. Lead é intenção de clique, não membro.

Index3baseline/candidato byte a byte idênticos àQAvisual25nov390×844/360×800 (hashesconferidos); nenhuma nova implementação/captura/Safari/WebVitals alegada. NodeVMatual produção/proposta/controle:10casos+href/constantePASS,delay150ms/Lead antesdenavegação, zeroeventoMeta/join/mensagem. Prova20.000/estrelas não comprovada; pedidos anteriores pendentes, sem cobrança repetida.

Execução27novcompleted, reciboTelegram21933 ehashdarespostafinalextraída verificados; incidente23outresolved,24novambíguo não reenviado. Hojeentrega somente após conclusão pela ponte, semenvio próprio. Agendaefetiva01hSP/04UTC,próxima29nov01hSP;nenhuma reconfiguração. Medir28nov completo ebackfill27nov, preservar fases eaguardar disposição explícita#16, não dias arbitrários.

## Métricas e diagnóstico integral da coleta atual

# CRO ICB — 28/nov/2026 | corte27/nov completo
**PASS:12/12 células MCP×Graph diário exatas;36/36 checks finais.** America/Sao_Paulo;28nov parcial excluído. Snapshot principal `2026-11-28T04:03:16.307968+00:00`. MCP oficial/protocolo`2025-11-25`/mesma conversa e sessão,schemas+conta+campos confirmados;GraphGET somente leitura. Nenhuma mensagem/Meta/GitHub/landing alterados.

## Totais ponderados reais
|Janela inclusiva|Campanha|Mídia R$|Impressões|Cliques link|LPV|Leads proxy|CVR% [Wilson95%]|CPL R$|
|---|---|---:|---:|---:|---:|---:|---:|---:|
|1d 2026-11-27–2026-11-27|Original index3|134.90|19242|478|398|145|36.43 [31.85;41.27]|0.9303|
|1d 2026-11-27–2026-11-27|Controle index4_li|251.52|28824|757|647|255|39.41 [35.72;43.23]|0.9864|
|1d 2026-11-27–2026-11-27|Clone index3 (separado)|117.08|15416|485|384|122|31.77 [27.31;36.59]|0.9597|
|3d 2026-11-25–2026-11-27|Original index3|417.44|68951|1690|1341|473|35.27 [32.76;37.87]|0.8825|
|3d 2026-11-25–2026-11-27|Controle index4_li|800.94|102000|2753|2319|917|39.54 [37.57;41.55]|0.8734|
|3d 2026-11-25–2026-11-27|Clone index3 (separado)|384.28|59647|1907|1512|433|28.64 [26.42;30.97]|0.8875|
|7d 2026-11-21–2026-11-27|Original index3|1004.26|180267|4431|3573|1312|36.72 [35.15;38.31]|0.7654|
|7d 2026-11-21–2026-11-27|Controle index4_li|1401.03|183071|5210|4406|1750|39.72 [38.28;41.17]|0.8006|
|7d 2026-11-21–2026-11-27|Clone index3 (separado)|581.47|100586|3011|2440|735|30.12 [28.33;31.97]|0.7911|
|14d 2026-11-14–2026-11-27|Original index3|2071.88|349124|9363|7648|2744|35.88 [34.81;36.96]|0.7551|
|14d 2026-11-14–2026-11-27|Controle index4_li|2460.73|330790|9407|7923|3095|39.06 [37.99;40.14]|0.7951|
|14d 2026-11-14–2026-11-27|Clone index3 (separado)|972.50|171056|4905|3985|1257|31.54 [30.12;33.00]|0.7737|

CVR=Leads/LPV e CPL=mídia/Leads dos totais; aliases selecionados, não somados. Lead=proxy de clique pré-navegação, **não membro confirmado**. Baseline36% semdenominador/data é apenas descritivo. Clone nunca somado àoriginal.

### Diferença Original−Controle
- 1d:-2.98p.p.;IC95%nominal[-9.02;3.06].
- 3d:-4.27p.p.;IC95%nominal[-7.51;-1.03].
- 7d:-3.00p.p.;IC95%nominal[-5.14;-0.86].
- 14d:-3.18p.p.;IC95%nominal[-4.70;-1.67].

## Diagnóstico novo e decisão
- Original recupera CVR diariamente sem novo tratamento. Não confundir recuperação de taxa com volume/eficiência sustentados nem avaliar contraste não publicado.
|Campanha|26nov CVR→27nov|ΔCVR p.p.|ΔCPL|ΔLPV|Δmídia|
|---|---:|---:|---:|---:|---:|
|Original index3|33.25→36.43%|3.18|-1.47%|-4.10%|3.53%|
|Controle index4_li|36.80→39.41%|2.61|5.01%|-9.13%|2.20%|
|Clone index3 (separado)|24.79→31.77%|6.98|-11.20%|-18.64%|-7.41%|

- O gap7d favorece controle nominalmente, mas não identifica efeito de landing/copy/orçamento: campanhas distintas, eventos atribuídos/dependentes e leituras sequenciais. Original tem CPL7d menor apesar de CVR menor, em contexto de CPM mais baixo. Não declarar vencedor/derrota, nem reabrirCRO001.
- Na fase26–27nov, retorno diário de CVR não recuperou a eficiência da referência20–24nov. Preservar25misto, fases14/17/19/23/25 e todos os dias, sem escolher só24nov ou suprimir dias ruins.
- Próxima ação CRO é decisão humana noPR16 e confirmaçãoPagesSHA+HTML pelo pai; depois congelar14dias pré-publicação/excluir dia misto/revalidar uma vez referência4170 conformeplano. Nenhum gate novo de volume/material ou mudançaMeta. Próxima rotina mede28nov completo e revisões27nov, sem promessa de estabilidade de reporting.

## Dois dias inteiros pós-orçamento versus cinco dias anteriores
Budgets externos25nov:controle150→300 às06:43:50SP;clone50→150 às06:44:55SP;original150 inalterado.25nov continua misto;26–27são dois dias completos.
|Campanha|LPV/dia20–24→26–27|Mídia/dia antes→depois R$|CVR antes→depois|CPL antes→depois|ΔCPL|
|---|---:|---:|---:|---:|---:|
|Original index3|541.20→406.50|142.932→132.600|36.95→34.81%|0.7147→0.9371|31.13%|
|Controle index4_li|511.00→679.50|148.882→248.810|39.57→38.04%|0.7363→0.9625|30.72%|
|Clone index3 (separado)|232.80→428.00|48.608→121.765|33.08→27.92%|0.6313→1.0190|61.41%|

Controle/clone entregam mais LPV/dia após aumento, mas mídia cresce mais; não comprova causa orçamentária ou canibalização. Original sem aumento tem menosLPV/dia. Calendário e fases distintas impedem inferência causal ou projeção proporcional ao orçamento.

### Contabilidade do CPL da fase26–27 versus20–24
Identidade verificada sem arredondar: CPL=CPM/(1000×CTRlink×LPV/clique×Lead/LPV). Componentes multiplicativos/log emJSON são aritmética descritiva, não causas independentes.
|Campanha|ΔCPM|ΔCTRlink|ΔLPV/clique|ΔCVR|ΔCPL|
|---|---:|---:|---:|---:|---:|
|Original index3|19.13%|0.42%|-3.95%|-5.81%|31.13%|
|Controle index4_li|10.63%|-12.21%|0.26%|-3.86%|30.72%|
|Clone index3 (separado)|42.69%|13.88%|-8.04%|-15.59%|61.41%|

## Semanas não sobrepostas14–20→21–27nov
|Campanha|Leads/LPV anterior→atual|CVR anterior→atual|Δp.p.[IC95%]|Δrelativa|ΔCPL|
|---|---:|---:|---:|---:|---:|
|Original index3|1432/4075→1312/3573|35.14→36.72%|1.58[-0.58;3.73]|4.49%|2.67%|
|Controle index4_li|1345/3517→1750/4406|38.24→39.72%|1.48[-0.68;3.64]|3.86%|1.61%|
|Clone index3 (separado)|522/1545→735/2440|33.79→30.12%|-3.66[-6.64;-0.68]|-10.84%|5.61%|
Diferença entre mudanças Original−Controle:0.10p.p.[-2.95;3.15];entre evoluçõesrelativas:0.63pontospercentuais. Descritivo,não causal.

## Configuração, exposição e atividades
- Sem novas mudanças semânticas de campanha/conjuntos/anúncios porID versus snapshot final27nov. União deIDs mantida. Diferença bruta no anúncioantigo pausado é somente miniaturaassinada; não é novaedição. Drafts atuais0.
- Todas campanhas OUTCOME_LEADS/LOWEST_COST_WITHOUT_CAP; conjuntos OFFSITE_CONVERSIONS, promoted_object Pixel1504398471438133/custom_event_typeLEAD, cobrançaIMPRESSIONS. destination_typeUNDEFINED não sobrepõe os links explícitos dos criativos.
- Original/controle atribuição7dclick+1dview+1dengaged-video;clone7dclick+1dview. MCP e todos adsets confirmam. URLtags e tracking_specs completos preservados nosraws/JSON.
- Original index3:campanhaACTIVE,R$150/dia;status efetivos{"PAUSED": 3, "ACTIVE": 2};issues retornados0.
  - Ad`120251541120490505`/criativo`1161944266575059`→https://lidimelo.com.br/index3.html.
  - Ad`120252297350870505`/criativo`2282920992488231`→https://lidimelo.com.br/index3.html.
  - Conjunto`120250764485200505`:ACTIVE/ACTIVE;targeting e attribution_spec integrais emsummary.json.
- Controle index4_li:campanhaACTIVE,R$300/dia;status efetivos{"ACTIVE": 1};issues retornados0.
  - Ad`120250926403940505`/criativo`1649512879970621`→https://www.lidimelo.com.br/index4_li.html.
  - Conjunto`120250926396700505`:ACTIVE/ACTIVE;targeting e attribution_spec integrais emsummary.json.
- Clone index3 (separado):campanhaACTIVE,R$150/dia;status efetivos{"PAUSED": 3, "ACTIVE": 1, "ADSET_PAUSED": 2};issues retornados0.
  - Ad`120252802517800505`/criativo`2460602314747134`→https://lidimelo.com.br/index3.html.
  - Conjunto`120252802517710505`:ACTIVE/ACTIVE;targeting e attribution_spec integrais emsummary.json.
  - Conjunto`120252642175430505`:PAUSED/PAUSED;targeting e attribution_spec integrais emsummary.json.
- Graph134atividades/2páginas exauridas;0novas edições relevantes dascampanhas;MCP13atividades desde25nov, semcontinuação/cursor pendente. Comparação deidentidade ignora só mudança deURLassinado em payloadhistórico.
- **Novo evento de cobrança da conta**:2026-11-27T23:22:42-03:00,R$250.85,transação`29704698535882308-29577182011967287` corroborada Graph/MCP. Não é mídia deuma campanha nem prova deaumento de orçamento, imposto oucausa deCVR.
- **Novo evento de cobrança da conta**:2026-11-27T14:13:16-03:00,R$250.31,transação`29516740084678152-29497385846613577` corroborada Graph/MCP. Não é mídia deuma campanha nem prova deaumento de orçamento, imposto oucausa deCVR.

## Distribuição7d conciliada — não diagnósticoSafari
|Campanha|Segmento|LPV|Lead proxy|ShareLPV|CVR|CPL R$|
|---|---|---:|---:|---:|---:|---:|
|Original index3|android_smartphone|2114|877|59.17%|41.49%|0.7360|
|Original index3|android_tablet|1|1|0.03%|100.00%|0.9300|
|Original index3|desktop|0|0|0.00%|—%|—|
|Original index3|ipad|0|0|0.00%|—%|—|
|Original index3|iphone|1458|434|40.81%|29.77%|0.8236|
|Original index3|other|0|0|0.00%|—%|—|
|Original index3|feed/instagram|202|110|5.65%|54.46%|0.6414|
|Original index3|instagram_explore_grid_home/instagram|2|0|0.06%|0.00%|—|
|Original index3|instagram_reels/instagram|235|86|6.58%|36.60%|0.7264|
|Original index3|instagram_search/instagram|0|0|0.00%|—%|—|
|Original index3|instagram_stories/instagram|3134|1116|87.71%|35.61%|0.7801|
|Controle index4_li|android_smartphone|2570|1109|58.33%|43.15%|0.7999|
|Controle index4_li|android_tablet|3|0|0.07%|0.00%|—|
|Controle index4_li|ipad|1|2|0.02%|200.00%|0.2050|
|Controle index4_li|iphone|1832|639|41.58%|34.88%|0.8010|
|Controle index4_li|other|0|0|0.00%|—%|—|
|Controle index4_li|feed/instagram|863|409|19.59%|47.39%|0.7830|
|Controle index4_li|instagram_explore_grid_home/instagram|4|2|0.09%|50.00%|1.1200|
|Controle index4_li|instagram_reels/instagram|409|166|9.28%|40.59%|0.7067|
|Controle index4_li|instagram_search/instagram|4|3|0.09%|75.00%|0.2400|
|Controle index4_li|instagram_stories/instagram|3126|1170|70.95%|37.43%|0.8209|
|Clone index3 (separado)|android_smartphone|2234|669|91.56%|29.95%|0.7879|
|Clone index3 (separado)|android_tablet|2|1|0.08%|50.00%|0.5601|
|Clone index3 (separado)|ipad|0|0|0.00%|—%|—|
|Clone index3 (separado)|iphone|204|65|8.36%|31.86%|0.8269|
|Clone index3 (separado)|other|0|0|0.00%|—%|—|
|Clone index3 (separado)|feed/facebook|1967|569|80.61%|28.93%|0.7825|
|Clone index3 (separado)|feed/instagram|117|35|4.80%|29.91%|1.0001|
|Clone index3 (separado)|instagram_explore_grid_home/instagram|0|0|0.00%|—%|—|
|Clone index3 (separado)|instagram_reels/instagram|99|33|4.06%|33.33%|0.7901|
|Clone index3 (separado)|instagram_stories/instagram|257|98|10.53%|38.13%|0.7666|

Dispositivos/placements não são coortes únicas ou ajuste causal conjunto;não somar marginais. Não atribuir gap de aparelho aSafari. Controle24noviPad diário1LPV/2Lead mantém200% eWilson indefinido,mesmo que agregado7d permita intervalo.

## Qualidade, revisões e gates de leitura
- Todos12primários exatos emspend/impressões/cliques/LPV/Lead; todos ad-day/hourly27nov e delivery-only26–27conciliados.4marginais iniciais controle1d/7ddevice/placement tinham−R$0,02 comcontagensexatas; uma rodada limitada acrescentando time_increment1 recuperou soma exata/subcentavo. Inicialanalysis-initial.json e todosraws preservados,sem alterarprimárias,atribuição ou tolerâncias.
- Final36/36checks passam, incluindo7ddevice/placement; isto é consistência do snapshot, não prova deestabilidadefinal. Sem partial-read gate atual para métricas/hierarquia,sem cursor ounext_action relevante pendente.
- Falha suplementar inicial JSONDecodeError/HTTPerrorbodyvazio preservada; retry emnomesnovos completou configuração/delivery-only. Nenhumtoken exposto ou aprovaçãoalterada.
- Revisões de26nov versus snapshotfinal27nov:
- experimental 2026-11-26:{"spend": {"previous": "130.28", "current": "130.3"}, "impressions": {"previous": 21916, "current": 21923}}. LPV/Leadinalterados.
- controle 2026-11-26:{"spend": {"previous": "245.99", "current": "246.1"}, "impressions": {"previous": 31136, "current": 31147}}. LPV/Leadinalterados.
- clone 2026-11-26:{"spend": {"previous": "125.39", "current": "126.45"}, "impressions": {"previous": 19703, "current": 19870}}. LPV/Leadinalterados.
- Limitaçãohistórica:IDfirst-delivery120252802586720505 permanece não identificado, jáencaminhado; não equivale a falha na enumeração atual ou gastooculto.
- GitHub/publicação/QA/diário são escopo dopai. CRO001Inconclusivo permanece fechado;CRO002não publicado conforme contexto/histórico. Nenhumganhodeconversão atribuído aocontraste.

## Artefatos
- `summary.json`: análiseauditável integral,coberturas,configuração,destinos,atribuição,semanas,fases,contabilidadeCPL echecks.
- `result.json`: payloadcompacto paraopai;`report.md`: estedocumento.
- `analysis-initial.json`,`analysis-bounded.json`,`selected-bounded.json`: snapshots e seleção explícita de4releituras.
- `raw/`:requests/responses imutáveis.MCPsession/protocollocais não fazempartedomanifesto;token ficaapenas emsecret.
- `manifest.json`,`acceptance.json`:hashes eaceitaçãoindependente.Não regenerar/reescrever estesarquivos;verificador dopai deve sersomenteleitura ouusar outrodiretório.
