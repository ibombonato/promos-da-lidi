# 27/nov — decisão humana separada de CI e risco verificado das propostas de rota

## Resultado técnico novo, não outro experimento

CRO-002 permanece Em PR #16 e não publicado; CRO-001 encerrado Inconclusivo. A preparação do contraste ocorreu há 35 dias civis. Esta auditoria não coletou Meta, não atribui lift, não cobra novamente materiais e não muda o plano4170/primáriaLead-LPV.

**Fontes pinadas:** main `79133f0fdddbfc64cd1c84ac0465c41a27eadf70`, PR16 `378a0f439f598b7bf9a3978624e19e41734bf11c`, árvore prospectiva `6cb68a8c64dd6da09bb682516649903b3f561a61`. GETs completos com paginação armazenados em prep-*.json; provas adicionais em decision-gate-diagnostic.json e prospective-pr-*.log.

### Bloqueio que foi efetivamente testado

- PR16 não é draft; APImergeable_state=clean, merge-treeexit0. Resultado index3 é EXATAMENTE main+duascores, controle/rotas/scripts/copys humanos preservados. Nenhum conflito de integração encontrado nestes SHAs.
- No head exato há 0check-runs, 0contexts de status e 0Actions runs; status agregado pending sem contexts NÃO é um teste falhando ou workflow executando. Pagesbem-sucedido está na main, não é CI de PR. Não há evidência para esperar uma execução de PagesdoPR por conta própria.
- 0reviews, 0comentários da issue, 0comentários inline e nenhumreviewer/time solicitado. APIbranches/main retorna protected=false; rules/branches/mainHTTP200 devolve[]. EndpointprotectionHTTP403por escopo PAT limita inspeção integral; não diagnosticar falha de login, regra oculta específica ou permissão de merge a partir disso. Identidadeibombonato/permissãopush confirmadas, mas não autorizam esta execução a publicar.
- **Conclusão operacional:** não foi encontrado impedimento técnico exposto no#16; falta uma decisão explícita deibombonato (aprovar, pedir ajuste, rejeitar). Ausência de comentário não prova que ninguém tenha lido ou recusado. Não realizar merge/auto-merge, solicitarreview porAPI nem enviar mensagem.

### Risco de aprovação distinto, demonstrado em vez de presumido

- PR31 (sóURLsindex3): simulaçãoexit1/CONFLICT, preservada em prospective-pr-31.log. Intenção atual deve ser decidida pelo dono; não corrigir convite nem fechar oPR automaticamente.
- PR40 ePR41 (sóURLsindex.html, fora das duaslandings medidas): ambos simulamexit0 e **mudariam a rota atual para alternativas diferentes**. Nos dois casos, index.html da main atual voltou a ser byte a byte igual ao arquivo do merge-base. O merge de três vias portanto reaplica a proposta antiga sem conflito. Uma fila antiga pode estar tecnicamente clean por ciclo de URLs; isso não comprova que a intenção de negócio ainda seja atual.
- Rota atualindex.html `https://chat.whatsapp.com/LNEB1eY3T3WIirBxGsXTJE`; proposta40 `https://chat.whatsapp.com/J3kAFznZtCV9ure4rnRWJU`; proposta41 `https://chat.whatsapp.com/CoviDBnmyCK1zVAoowS5Ud`. Não concluir grupo cheio/inválido, nem seguir convite. #76/#77 acabaram de publicar a rota humana atual. Este caso é diferente de dizer que um head antigo sempre reverte main: aqui o efeito prospectivo foi calculado e está pinado.

## Contribuição concreta e hipótese operacional

**Hipótese:** separar na fila a decisão experimental#16 das propostas antigas#31/#40/#41, mostrando rota/arquivo e efeito de merge prospectivo, reduz aprovação equivocada de destinos e elimina a falsa espera por CI inexistente. **ICE qualitativo I7/C9/E8**: impacto sobre segurança/fluxo de aprovação; confiança9 é na existência do risco técnico demonstrado, NÃO em efeito deCVR. Não criarIDCRO.

**Teste/aceitação:** (1) pinarmain/head, (2) PR16exatamente2cores/controlpreservado e semconflicto, (3) PR31conflict, (4) PR40/41cleanmasrotasdistintas apósretornoaomerge-base, (5) zeroHEAD/refsmovidas. Esses casos passaram nesta auditoria. Reexecutar se main/head mudar. Sucesso de negócio só após decisão humana registrada; redução de tempo/erros não foi medida. Não repetir simplesmente o títuloBL-02nem inventar gateestatístico novo.

**Handoff ao responsável — registrado no PR e relatório, sem mensagem direta:** ibombonato decidir somente#16 com escopo atual verificado; conferir separadamente se ainda deseja os destinos antigos#31/#40/#41. Após eventual merge humano, confirmar novoPagesSHA+status+HTML e congelar14diasanteriores/excluir diamixto/revalidarumavez4170conformeplano. Não ampliar autorização para Meta/links/mensagens.

## Publicação e QA atual

Mainpublicada: deployment8100580176success2026-11-27T02:54:01Z (2026-11-26T23:54:01-03:00), Actions45930958360success; ambaslandingsHTTP200eHTMLbyteabyteiguaisàmain. Coresantigas: CRO-002não começou. Último delta desde26nov é somente convites do controle/index.html; index3inalterado. Rotação não reseta Lead/LPV e publicação tardia do controle não é tratamento visível.

Fontebaseline/candidatoindex3idêntica àQA25nov, hashes atuais conferem; nenhuma nova captura ouSafari/WebVitalsalegados, nenhuma QAvisualnova requerida para uma proposta experimental inalterada. NodeVM atual emprodução/proposta/controle:10casoscomportamentais+href/constantePASS,delay150ms/Lead antesdanavegação normal, zeroeventoreal/join. Se futura rotação alterar fonteindex3, pedir QAde fonteatual antes de envio; não confundir normalizaçãoURL comrenderização atual.

Worktree preparada em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-11-27/repo` na branch `docs/cro-monitor-2026-11-27`, HEADaindamain, semindexstage/commit/push. CRO_EXPERIMENTS.md está copiado integralmente doresultado prospectivo (idêntico aoheadPR16), sem qualquer entrada27nov/edição histórica adicionada. Diário fica aoagenteprincipal. Conteúdohumano20.000/estrelas preservado,nãocomprovado.


## Medição atual e limitação de reporting

# CRO ICB — 27/nov/2026 | corte 26/nov completo

**PRIMARY_PASS_BREAKDOWN_PARTIAL** — 12/12 células MCP×Graph diário exatas; 24/30 checks totais. Conta974182265670621, BRL, America/Sao_Paulo. Hoje27/nov parcial excluído. Coleta em `2026-11-27T04:08:05.798207+00:00`; atualizações marginais posteriores identificadas separadamente.

## Métricas reais — campanhas separadas
|Janela inclusiva|Campanha|Mídia R$|Impressões|Cliques link|LPV|Lead proxy|CVR% [Wilson95%]|CPL R$|
|---|---|---:|---:|---:|---:|---:|---:|---:|
|1d 2026-11-26 a 2026-11-26|Original index3|130.28|21916|552|415|138|33.25 [28.89;37.92]|0.9441|
|1d 2026-11-26 a 2026-11-26|Controle index4_li|245.99|31136|843|712|262|36.80 [33.34;40.40]|0.9389|
|1d 2026-11-26 a 2026-11-26|Clone index3 — separado|125.39|19703|629|472|117|24.79 [21.11;28.88]|1.0717|
|3d 2026-11-24 a 2026-11-26|Original index3|412.24|70835|1749|1385|486|35.09 [32.62;37.64]|0.8482|
|3d 2026-11-24 a 2026-11-26|Controle index4_li|682.94|89124|2512|2103|840|39.94 [37.87;42.05]|0.8130|
|3d 2026-11-24 a 2026-11-26|Clone index3 — separado|311.23|51256|1663|1335|395|29.59 [27.20;32.09]|0.7879|
|7d 2026-11-20 a 2026-11-26|Original index3|997.18|181859|4505|3649|1328|36.39 [34.85;37.97]|0.7509|
|7d 2026-11-20 a 2026-11-26|Controle index4_li|1293.72|172412|5012|4227|1673|39.58 [38.11;41.06]|0.7733|
|7d 2026-11-20 a 2026-11-26|Clone index3 — separado|509.18|94313|2815|2292|696|30.37 [28.52;32.28]|0.7316|
|14d 2026-11-13 a 2026-11-26|Original index3|2076.19|348907|9539|7760|2793|35.99 [34.93;37.07]|0.7434|
|14d 2026-11-13 a 2026-11-26|Controle index4_li|2353.19|325306|9228|7754|3022|38.97 [37.89;40.06]|0.7787|
|14d 2026-11-13 a 2026-11-26|Clone index3 — separado|854.36|155473|4420|3601|1135|31.52 [30.02;33.06]|0.7527|

CVR/CPL calculados dos totais, nunca média de taxas; aliases LPV/Lead selecionados, não somados. Lead é intenção de clique pré-redirecionamento, **não participante confirmado**. Atribuição unificada: original/controle7dclick+1dview+1dvídeoengajado; clone7dclick+1dview.

### Diferença Original−Controle
- 1d: -3.54p.p.; IC95%normal[-9.30;2.21].
- 3d: -4.85p.p.; IC95%normal[-8.12;-1.58].
- 7d: -3.19p.p.; IC95%normal[-5.33;-1.04].
- 14d: -2.98p.p.; IC95%normal[-4.50;-1.46].

## Novidade desde26/nov: primeiro dia civil completo pós-orçamento
Aumentos externos foram25/nov06:43:50SP no controle150→300 e06:44:55SP no clone50→150. Original150 inalterado. Dia25 continua **misto**; dia26 é primeiro inteiro, não novo tratamentoCRO.
|Campanha|25nov CVR→26nov|ΔCVR p.p.|ΔCPL|ΔLPV|Δmídia|
|---|---:|---:|---:|---:|---:|
|Original index3|35.98→33.25%|-2.73|17.82%|-21.40%|-14.42%|
|Controle index4_li|41.67→36.80%|-4.87|23.82%|-25.83%|-18.90%|
|Clone index3 — separado|29.57→24.79%|-4.79|47.72%|-28.05%|-10.91%|

Comparar também com referência20–24nov(5dias inclusivos), sem selecionar24nov isolado:
|Campanha|LPV/dia20–24→26|Mídia/dia20–24→26 R$|CVR20–24→26|CPL20–24→26|
|---|---:|---:|---:|---:|
|Original index3|541.20→415|142.932→130.28|36.95→33.25%|0.7147→0.9441|
|Controle index4_li|511.00→712|148.882→245.99|39.57→36.80%|0.7363→0.9389|
|Clone index3 — separado|232.80→472|48.608→125.39|33.08→24.79%|0.6313→1.0717|

Controle/clone ainda têm entrega superior à média pré-aumento, mas eficiência26nov pior. Um dia não identifica efeito do orçamento, landing, mix ou canibalização. Não projetar volume proporcional ao orçamento. Orçamento diário não é teto rígido; mídia não inclui impostos/cobrança. Fases14/17/19/23/25nov e todos os snapshots preservados em JSON; não reiniciar baseline/endpoint.

## Semanas não sobrepostas13–19 →20–26nov
|Campanha|Lead/LPV antes→agora|CVR antes→agora|Δp.p. [IC95%normal]|Δrelativa|CPL antes→agora|
|---|---:|---:|---:|---:|---:|
|Original index3|1465/4111→1328/3649|35.64→36.39%|0.76 [-1.38;2.90]|2.13%|0.7365→0.7509|
|Controle index4_li|1349/3527→1673/4227|38.25→39.58%|1.33 [-0.85;3.51]|3.48%|0.7854→0.7733|
|Clone index3 — separado|439/1309→696/2292|33.54→30.37%|-3.17 [-6.35;0.01]|-9.45%|0.7863→0.7316|

Diferença entre mudanças Original−Controle -0.57p.p.[-3.63;2.48]; entre evoluções relativas -1.35pontos percentuais. Campanhas/eventos atribuídos não randomizados, dependentes e consultas sequenciais: **descrição, não causalidade**. Semana inicial do clone inclui13nov sem entrega; médias civis não significam7dias ativos.

## Qualidade, revisões e configuração
- Quatro snapshots completos e três consultas dirigidas finais preservados. Inicial falhou em LPV e impressões marginais; reconsultas mostraram backfill controle705/260→712/262, clone471→472LPV e19700→19703impressões. Sem relaxar igualdade dos contadores ou substituir por números antigos.
- No snapshot primário final todas12células de1/3/7/14dias conciliam gasto/impressões/cliques/LPV/Lead exatamente. Todos os ad-day finais também conciliam. Resíduos de allocation menores que1centavo são permitidos sóem breakdowns; diferenças exatas remanescentes abaixo não passam:
- **FAIL breakdown-clone-publisher_platform-platform_position**: {"spend": "0.010000", "impressions": "2", "clicks": "0", "lpv": "0", "leads": "0"}.
- **FAIL breakdown7d-experimental-impression_device**: {"spend": "0.00", "impressions": "0", "clicks": "0", "lpv": "-1", "leads": "0"}.
- **FAIL breakdown7d-experimental-publisher_platform-platform_position**: {"spend": "0.00", "impressions": "0", "clicks": "0", "lpv": "-1", "leads": "0"}.
- **FAIL breakdown7d-controle-publisher_platform-platform_position**: {"spend": "0.000000", "impressions": "-1", "clicks": "0", "lpv": "-7", "leads": "-2"}.
- **FAIL breakdown7d-clone-impression_device**: {"spend": "0.010000", "impressions": "2", "clicks": "0", "lpv": "0", "leads": "0"}.
- **FAIL breakdown7d-clone-publisher_platform-platform_position**: {"spend": "0.010000", "impressions": "2", "clicks": "0", "lpv": "0", "leads": "0"}.
- Esses breakdowns são diagnósticos provisórios; não recalcular taxas da campanha por somas marginais divergentes nem afirmar consistência total/estabilidade de reporting. Dispositivos/placements1d e7d ficam no JSON com respectivos checks; não diagnosticarSafari.
- Revisões históricas versus raw26nov, preservando snapshot anterior:
- experimental 2026-11-25: {"spend": {"prior": "152.22", "current": "152.24"}, "impressions": {"prior": 27782, "current": 27786}, "lpv": {"prior": 525, "current": 528}, "leads": {"prior": 188, "current": 190}}.
- controle 2026-11-25: {"spend": {"prior": "303.24", "current": "303.32"}, "impressions": {"prior": 42020, "current": 42029}, "clicks": {"prior": 1152, "current": 1153}}.
- clone 2026-11-25: {"spend": {"prior": "139.55", "current": "140.75"}, "impressions": {"prior": 24110, "current": 24361}, "clicks": {"prior": 788, "current": 793}}.
- Original index3: campanhaACTIVE, orçamentoR$150, roster{"PAUSED": 3, "ACTIVE": 2}; issues retornados0.
- Controle index4_li: campanhaACTIVE, orçamentoR$300, roster{"ACTIVE": 1}; issues retornados0.
- Clone index3 — separado: campanhaACTIVE, orçamentoR$150, roster{"PAUSED": 3, "ACTIVE": 1, "ADSET_PAUSED": 2}; issues retornados0.
- Configurações porID sem novas alterações semânticas versus26nov; copy, destinos explícitos, Pixel/UTMs/atribuição preservados. Única diferença raw: thumbnail assinado do anúncio antigo pausado. Destinosoriginal/cloneindex3 econtroleindex4_li confirmados. Drafts atuais:0.
- Graph activities: 132registros/2páginas exauridas. Quatro payloads históricos de14/17nov diferem porURLs assinadas: isso **não é nova edição**. Comparação por(event_time,event_type,object_id,object_type) em `activity-audit.json` separa eventos novos de variações de payload. MCP activities:11 registros(limit1000), consulta25–27nov; nenhuma alteração Meta inferida só porpayload diferente.


**Próxima observação:** reconsultar seis marginais divergentes e o backfill26nov;27nov completo na rotina28nov01hSP. Nenhuma marginal divergente substitui as12células primárias conciliadas. Sem atribuir a piora ao orçamento/copy ou resetar endpoint.
