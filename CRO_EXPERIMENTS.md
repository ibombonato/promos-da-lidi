# Histórico de experimentos CRO — ICB

> **Atualização vigente — 2026-10-31:** CRO-002 **Em PR #16, não publicado**; CRO-001 encerrado Inconclusivo. Entrega concreta: BL-02 prototipado exclusivamente offline, avanço129px da oferta/CTA confirmado em390/360, sem ganho de CVR alegado. Experimental teve segundo dia completo de entrega retomada(638LPV), mas CVR35,27%; causa28/out ainda desconhecida. Gate é decisão humana no#16 e confirmaçãoPagesSHA+HTML, não volume doCRO-001. Controle rotacionado externamente em30/out, preservado na branch.

> **Atualização vigente — 2026-10-30:** CRO-002 continua **Em PR #16, não publicado**; CRO-001 encerrado Inconclusivo. **Retomada experimental em um dia completo confirmada:**29/out R$171,99/711LPV/276Leads; volume próximo de27/out, causa da interrupção28/out ainda desconhecida. Entrega concreta: conciliação horária e decomposição de mix27→29/out, sem mudança na landing. Novos anúncios agora44,73% dosLPV. Gate: decisão humana no#16 e confirmaçãoPagesSHA+HTML, não mais volumeCRO-001. Preservados o dia de subentrega e todos os registros anteriores.

> **Atualização vigente — 2026-10-29:** CRO-002 continua **Em PR #16, não publicado**; CRO-001 permanece encerrado Inconclusivo. **Alerta de entrega:** experimental gastou só R$2,80 e recebeu16LPV em28/out, queda de97,84% dos LPV versus27/out, confirmada por MCP e Graph. Entrega concreta: diagnóstico horário/hierarquia/erros e encaminhamento a ibombonato; causa ainda não identificada, sem alterações Meta/HTML. Decisão humana no#16 segue pendente; não avaliar CVR com apenas16LPV nem extrapolar a antiga projeção de volume. Registros anteriores preservados.

> **Atualização vigente — 2026-10-28:** CRO-002 continua **Em PR #16, não publicado**; CRO-001 encerrado Inconclusivo. Novidade externa: controleR$170→150/dia em27/out09:47:50SP, dia misto; experimentalR$150inalterado. Entrega: viabilidade exploratória offlineBL-06 medida em390/360, sem editar landing/PR ou iniciar tratamento paralelo. Gate: decisão humana no#16 e confirmaçãoPagesSHA+HTML. Histórico anterior preservado.

> **Atualização vigente — 2026-10-27:** CRO-002 permanece **Em PR #16, não publicado**; CRO-001 encerrado Inconclusivo. Entrega: decomposição verificável da variação diária e refinamento do plano BL-02 com sensibilidade de mix pré-especificada, sem novo tratamento. Novos anúncios agora17,59% dos LPV do dia; não atribuir recuperação ao contraste ainda não publicado. Gate: decisão humana no#16 e confirmaçãoPagesSHA+HTML; preservados registros anteriores.

> **Atualização vigente — 2026-10-26:** CRO-002 continua **Em PR #16, não publicado**; CRO-001 encerrado Inconclusivo. Entrega: auditoria de divergência entre href sem query e URL JavaScript parametrizada introduzida na manutenção externa, testes comportamentais sem rede e encaminhamento ao responsável ibombonato; nenhuma correção de destino não autorizada. Main atual incorporada preservando rotas; o diff experimental continua somente duas cores CSS. Gate principal: decisão humana e publicação confirmada. Registros anteriores preservados.

> **Atualização vigente — 2026-10-25:** CRO-002 segue **Em PR #16, não publicado**; CRO-001 permanece encerrado Inconclusivo. Entregas: especificação do rótulo compacto BL-06, atualização segura da branch com convites operacionais já publicados e comprovação da retomada análise+Telegram de24/out (recibo18854). Nenhum tratamento adicional implementado. Decisão humana no#16 é o gate, não mais volume doCRO-001. Registros anteriores preservados.

> **Atualização vigente — 2026-10-24:** CRO-002 continua **Em PR** no#16 e **não publicado**, confirmado porPagesSHA+HTML; CRO-001 permanece encerradoInconclusivo. Entrega de hoje: especificaçãoBL-02 baseada emnova auditoria mobile, sem implementar outro tratamento. A análise automática voltou a executar; entrega deste relatório pela ponte só poderá ser confirmada por recibo após sua conclusão. Registros datados abaixo preservados.

> **Atualização vigente — 2026-10-23:** **CRO-002 Em PR**, teste isolado de contraste do CTA no PR#16. CRO-001 continua **Inconclusivo**, avaliação encerrada em22/out; não aguardar mais seu checkpoint. Nenhum merge/deploy realizado. Execução automática23/out falhou no gateway; análise real e implementação realizadas nesta sessão. Prompt diário corrigido; recuperação operacional/Telegram pendente de comprovação. Notas datadas abaixo são histórico preservado.

> **Atualização de 2026-10-22:** **CRO-001 encerrado como Inconclusivo** no checkpoint planejado, com 4346 LPV posteriores e cobertura semanal completa. Diferença entre mudanças +0,51 p.p., IC95% aproximado −1,97 a +2,99 p.p.; não foi comprovado benefício ou prejuízo. Manter a headline publicada, sem reversão ou novo tratamento nesta execução. Dois anúncios externos iniciaram entrega no fim de 21/out; acompanhar sua primeira jornada completa separadamente antes de preparar o próximo baseline. Publicação inicial confirmada em `1a377ea858b18189d7b40b1fd63990376e777712`, build concluído em 2026-10-13T23:42:37Z. Rotações operacionais não reiniciam avaliação. Registros e snapshots anteriores foram preservados; decisões antigas não são orientação vigente.

## Escopo e salvaguardas

- Repositório: `ibombonato/promos-da-lidi`; base de publicação: `main`.
- Experimental: `index3.html`; campanha `LEAD - Grupos - Criativo Validado Antigo — ICB` (`120250764485030505`).
- Controle: `index4_li.html`; campanha `LEAD - Grupos - Clone index4_li — ICB` (`120250926395490505`). O agente nunca deve modificar esse arquivo.
- Conta: `974182265670621`; moeda BRL; fuso **America/Sao_Paulo**.
- Meta Ads exclusivamente em leitura. Não alterar Pixel, eventos, parâmetros, destinos ou funcionalidades essenciais.
- Branch + PR com aprovação humana para qualquer alteração; nunca realizar merge, auto-merge ou deploy.
- Um experimento principal de cada vez. Antes de atuar, ler este histórico integralmente, consultar PRs e confirmar a versão realmente publicada.

## Baseline e contrato de medição

**Baseline inicial informado: 36% de CVR.** Data, LPV e número de conversões desse baseline não foram fornecidos; portanto ele é uma referência histórica, não uma amostra para teste estatístico.

**CVR = Leads atribuídos / Landing Page Views × 100.** Na landing atual, `fbq("track", "Lead")` dispara no clique normal do CTA do WhatsApp. É uma **conversão proxy de intenção/clique**, não uma entrada confirmada no grupo. A ação `lead` retornada pela Meta foi conciliada com `offsite_conversion.fb_pixel_lead` em todos os dias consultados. Não somar esses aliases; igualmente não somar `landing_page_view` com `omni_landing_page_view`.

As duas campanhas usam Pixel `1504398471438133` e a mesma configuração de atribuição observada: clique de 7 dias, visualização de 1 dia e visualização engajada de vídeo de 1 dia. Consultas Graph usam `use_unified_attribution_setting=true`; o MCP oficial confirmou os totais das quatro janelas. Essa atribuição não constitui uma coorte deduplicada de visitantes: Leads podem ser revisados posteriormente, e LPV e Leads não são necessariamente pessoas únicas ou ações da mesma visita. Manter a definição e a configuração estáveis; registrar revisões, sem substituir silenciosamente valores anteriores.

Não declarar causalidade pela comparação entre campanhas distintas. Interpretar intervalos binomiais como aproximações descritivas: repetição de visitas, dependência entre observações, atribuição e composição do tráfego podem limitar sua validade.

## Estado inicial confirmado em 2026-10-13

- O arquivo `CRO_EXPERIMENTS.md` não existia em `main`; inicialização nesta branch de acompanhamento, **pendente de merge humano**.
- Histórico dos PRs abertos/fechados consultado. Nenhum PR aberto encontrado antes da execução; não foi encontrado experimento CRO formal em avaliação. Isso não permite presumir resultados de alterações antigas.
- Publicação confirmada pela API Pages: commit `ea788ca10672f0c37b0da49b1241ac5a5bfc36e3`, build concluído em **2026-10-13T19:50:46Z** (16:50:46 no fuso da conta). A [execução Pages](https://github.com/ibombonato/promos-da-lidi/actions/runs/38457996221) terminou com sucesso.
- HTML público de ambas as landings retornou HTTP 200 e conferiu byte a byte com os arquivos desse commit; a mera existência de um PR não foi usada como prova de publicação.
- `index3.html` teve trocas de convite em 2026-10-12 (commits `166faca` e `c85b886`) e 2026-10-13 (`c294e85`, integrado no [PR #14](https://github.com/ibombonato/promos-da-lidi/pull/14)). `index4_li.html` também teve troca de convite por outro autor em 2026-10-12 (`c28a41c`). Nenhum desses destinos foi alterado por esta execução.
- Portanto, as janelas encerradas em 2026-10-12 **não avaliam a versão publicada em 2026-10-13**. Trocas de grupo podem afetar a etapa posterior ao clique e a comparabilidade; não são evidência de ganho de copy/layout.
- O [PR #3](https://github.com/ibombonato/promos-da-lidi/pull/3), integrado em 2026-08-07, tornou o CTA explícito. Não há métricas antes/depois ou publicação histórica suficientemente documentadas para classificá-lo como vencedor/perdedor. Não repetir essa hipótese como se o CTA atual fosse ambíguo.

## Estado dos experimentos na primeira análise — superado pelo CRO-001 abaixo

Nenhum experimento novo foi implementado na primeira análise desta execução. Essa decisão foi revisada após o esclarecimento operacional; o novo **CRO-001** está registrado ao fim deste arquivo. Não atribuir IDs retrospectivos ou resultados inventados a PRs antigos.

Cada registro deve conter ID sequencial; criação e publicação real; status (Proposto, Em PR, Em avaliação, Vencedor, Perdedor ou Inconclusivo); problema/hipótese/evidências; mudança objetiva; métricas antes e depois para ambas as campanhas; períodos exatos; impacto absoluto e relativo; incertezas, conclusão e aprendizados; PR, commit de publicação e screenshot mobile 390×844. Atualizar sem apagar registros anteriores. Dados posteriores ficam pendentes até a publicação confirmada; nenhum experimento é vencedor só porque subiu num dia.

## Diagnóstico inicial de 2026-10-13 — dados preservados; justificativa de espera corrigida abaixo

### Fontes e períodos

Coleta em 2026-10-13, aproximadamente 22:32–22:44 UTC. Fontes: **MCP oficial Meta Ads**, `ads_get_ad_accounts`, `ads_get_field_context`, `ads_get_ad_entities` somente leitura; Graph Marketing API GET para série diária, anúncios, atribuição e breakdowns; API GitHub/Pages e HTML público para histórico/publicação. Os totais de investimento, impressões, cliques, LPV e Leads do MCP foram conciliados exatamente com a soma dos dias do Graph em todas as quatro janelas.

Excluir 2026-10-13, ainda parcial no fuso da conta. CVR e CPL são calculados a partir dos totais (não média simples de taxas diárias). CPL é custo por Lead proxy; não custo por participante confirmado.

| Janela | Período completo inclusivo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 dia(s) | 2026-10-12 a 2026-10-12 | Experimental | R$ 109,20 | 26319 | 625 | 533 | 211 | 39,59% | R$ 0,52 |
| 1 dia(s) | 2026-10-12 a 2026-10-12 | Controle | R$ 217,60 | 63943 | 1360 | 1147 | 428 | 37,31% | R$ 0,51 |
| 3 dia(s) | 2026-10-10 a 2026-10-12 | Experimental | R$ 322,76 | 70241 | 1656 | 1410 | 517 | 36,67% | R$ 0,62 |
| 3 dia(s) | 2026-10-10 a 2026-10-12 | Controle | R$ 651,52 | 171400 | 3731 | 3148 | 1153 | 36,63% | R$ 0,57 |
| 7 dia(s) | 2026-10-06 a 2026-10-12 | Experimental | R$ 648,06 | 152871 | 3520 | 2969 | 1055 | 35,53% | R$ 0,61 |
| 7 dia(s) | 2026-10-06 a 2026-10-12 | Controle | R$ 1049,12 | 279860 | 6146 | 5177 | 1927 | 37,22% | R$ 0,54 |
| 14 dia(s) | 2026-09-29 a 2026-10-12 | Experimental | R$ 1162,06 | 257139 | 6354 | 5387 | 1992 | 36,98% | R$ 0,58 |
| 14 dia(s) | 2026-09-29 a 2026-10-12 | Controle | R$ 1568,22 | 384725 | 8993 | 7672 | 2901 | 37,81% | R$ 0,54 |

### Incerteza e evolução comparativa

- Nos 7 dias, experimental **35,53%**, IC95% Wilson **33,83%–37,27%**; controle **37,22%**, IC95% **35,92%–38,55%**.
- Diferença experimental menos controle: **−1,69 p.p.**; IC95% normal aproximado para proporções independentes **−3,86 a +0,48 p.p.** Inclui zero; não comprova superioridade/inferioridade da landing ou efeito causal.
- Experimental versus baseline informado de 36%: **−0,47 p.p.**, **−1,29% relativo** nos 7 dias. Sem denominador do baseline, não há teste estatístico válido contra ele.
- Comparar semanas não sobrepostas: 2026-09-29 a 2026-10-05 versus 2026-10-06 a 2026-10-12. Experimental: 937/2418 (**38,75%**) → 1055/2969 (**35,53%**), **−3,22 p.p. / −8,30% relativo**. Controle: 974/2495 (**39,04%**) → 1927/5177 (**37,22%**), **−1,82 p.p. / −4,65% relativo**.
- Diferença entre evoluções relativas: **−3,65 pontos percentuais de variação relativa**; diferença entre mudanças absolutas de CVR: **−1,40 p.p.** Descrição observacional, não estimativa causal de um experimento.
- A queda em ambas sugere investigar fatores comuns, mas não prova qual foi a causa. A recuperação experimental de ontem para 39,59% também não comprova melhoria sustentável.

### Tráfego e limitações de comparação

- Nome da campanha experimental não descreve o criativo efetivamente veiculado: há dois anúncios ativos (`120251541120490505`, produtos atualizados, e `120250848857170505`, texto 4 em 1); o criativo antigo `120250764534590505` está pausado. No controle há um ativo (`120250926403940505`), apesar de o nome conter “PAUSADO”. Estado efetivo, não nome, orientou a leitura.
- Destinos dos anúncios ativos conferidos: experimental `https://lidimelo.com.br/index3.html`; controle `https://www.lidimelo.com.br/index4_li.html`. Nenhuma URL/UTM alterada.
- Atualizações de conjuntos observadas em 2026-10-08 e de campanhas em 2026-10-08/09. Os timestamps não estabelecem sozinhos quais configurações mudaram; não atribuir a eles uma causa específica sem histórico de atividade.
- Nos 7 dias, LPV/clique: experimental **84,35%**, controle **84,23%**; não há evidência de falha grosseira de carregamento exclusiva da experimental. Isso não substitui métricas reais de Web Vitals.
- Dispositivos, 7 dias: Android smartphone experimental **738/1939 = 38,06%**, controle **1291/3261 = 39,59%**; iPhone experimental **316/1028 = 30,74%**, controle **634/1910 = 33,19%**. iPhone apresenta menor CVR nas duas campanhas; isso não comprova defeito específico de Safari ou da landing.
- Instagram Stories: experimental **892/2575 = 34,64%**, controle **1659/4585 = 36,18%**. Feed: **131/301 = 43,52%** versus **174/375 = 46,40%**. Reels: **32/93 = 34,41%** versus **93/213 = 43,66%**; volume menor, interpretação cautelosa. A distribuição não é equivalente.
- Ambos otimizam para LEAD; configurações observadas são semelhantes, mas os dispositivos/geolocalização, criativos, distribuição, investimento e volumes não são idênticos. Não modificar o Meta para “corrigir” a comparação.

### Auditoria técnica e mobile da versão publicada

- Chromium real; screenshots **390×844** e **360×800**, inspecionados visualmente. É emulação de viewport no Linux, não validação em Safari/iPhone real.
- CTA inteiro na primeira dobra: em 390×844, y **501,125–563,125**, largura 346 e altura 62 px; em 360×800, y **497,141–557,141**, largura 316 e altura 60 px. Texto em duas linhas, sem corte. Sem overflow horizontal em ambos.
- Rolagem 360×800 até o fim validada; grid de seis benefícios íntegro. Nenhuma exceção JavaScript observada nessa navegação; foto carregou, HTTP 200, 90062 bytes. Não foi medida performance de campo.
- Testes isolados do script real do CTA em Node VM: **11 verificações aprovadas**, incluindo fallback href/constante, Pixel/PageView sem Lead no carregamento, clique com tracking presente/ausente/com erro, atraso de 150 ms, modificadores, botão central/direito e evento já cancelado. Nenhum evento real de QA ou entrada no WhatsApp foi enviado.
- Navegação de auditoria bloqueou `facebook.com` e `facebook.net` antes de carregar a página; não poluiu tracking. O convite público retornou HTTP 200, mas isso **não verifica capacidade do grupo, aprovação ou entrada efetiva**.
- Contraste do texto branco do CTA contra as extremidades do gradiente: **2,38:1** (`#0bc247`) e **3,15:1** (`#09a83a`). Em mobile, o texto tem aproximadamente 15–16 px; a referência [WCAG 1.4.3](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) exige 4,5:1 para texto normal. É uma oportunidade objetiva de acessibilidade; não há prova de impacto na CVR.
- A landing já exibe “Mais de 16.000” e estrelas. Nenhuma comprovação desse número/avaliações foi localizada neste histórico; não tratar como prova social validada, ampliar ou reutilizar em novas peças sem evidência do responsável. Nenhuma afirmação nova foi criada.

**Screenshots da versão atual (não de experimento):**

![Baseline experimental 390×844](cro/screenshots/baseline-2026-10-13-390x844.png)

[Baseline 360×800](cro/screenshots/baseline-2026-10-13-360x800.png)

## Backlog da análise inicial — headline promovida ao CRO-001; contraste permanece separado

As notas ICE abaixo são julgamentos de priorização em escala 1–10, não resultados ou previsões estatísticas. Não implementar simultaneamente.

### 1. Clareza e correspondência anúncio–headline

- **Problema:** o headline “Nunca mais perca uma promoção!” é genérico; perfumes, marcas e canal só aparecem depois. Os anúncios ativos prometem explicitamente perfumes/Natura/O Boticário.
- **Evidência:** leitura da copy real dos anúncios ativos e da primeira dobra da landing; não há dados de scroll/atenção que comprovem abandono por esse motivo.
- **Proposta:** futuramente testar somente um headline que explicite promoções de perfumes/beleza no WhatsApp, mantendo CTA, destino, Pixel e demais argumentos. Não adicionar descontos ou promessas não comprovadas.
- **Justificativa/impacto esperado:** reduzir o esforço para entender se a oferta corresponde ao anúncio; potencial aumento de cliques no CTA por LPV.
- **ICE:** impacto 7, confiança 5, facilidade 9. Hipótese, não ganho previsto.
- **Avaliação:** CVR proxy com definição estável; CPL como secundária; distribuição por dispositivo/posicionamento e evolução do controle como contexto; publicação confirmada, janela anterior limpa e amostra suficiente, sem concluir só pelo tempo transcorrido.

### 2. Legibilidade do CTA

- **Problema/evidência:** contraste branco/verde abaixo de 4,5:1 na versão mobile.
- **Proposta:** em experimento separado, testar gradiente mais escuro, preservando texto, geometria, links, handler e tracking.
- **Justificativa/impacto esperado:** facilitar a leitura do comando, especialmente com baixa visão ou luz externa. Evidência técnica de contraste não é evidência de aumento de conversão.
- **ICE:** impacto 6, confiança 9 na existência do problema técnico (não no ganho de CVR), facilidade 9.
- **Avaliação:** contraste + QA mobile/funcional como gates; CVR como resultado; não misturar com mudança de headline.

## Diário de acompanhamento

Registros compactos por data de execução; adicionar novos registros cronologicamente, sem apagar histórico. A série retrospectiva abaixo é uma coleta em 2026-10-13, não execuções diárias realizadas no passado.

| Execução | Dia completo de referência | CVR experimental | CVR controle | LPV experimental / controle | Experimento | Decisão e observações |
|---|---|---|---|---|---|---|
| 2026-10-13 | 2026-10-12 | 39,59% | 37,31% | 533 / 1147 | Nenhum formal em avaliação | **Aguardar uma referência limpa da versão atual; não alterar landing.** Inicializar histórico e registrar dados. Destinos mudaram em 12/13-out; diferença 7d incerta e tráfego não randomizado. |
| 2026-10-14 — 09h São Paulo | 2026-10-13, dia misto excluído da avaliação principal | 38,34% | 36,87% | 459 / 990 | CRO-001 — Em avaliação | Manter landing: nenhum dia pós-tratamento completo ainda; publicação e baseline reconfirmados. Atualizar somente documentação no PR #16. |
| 2026-10-15 — 09h São Paulo | 2026-10-14, primeiro dia completo pós-publicação | 40,93% | 39,42% | 430 / 964 | CRO-001 — Em avaliação | Manter tratamento: resultado inicial inconclusivo, somente 10,42% do volume de planejamento; controle também subiu. Rotação operacional PR #17 não reinicia avaliação. Atualizar mesmo PR documental #16. |
| 2026-10-16 — 09h São Paulo | 2026-10-15, segundo dia completo pós-publicação | 41,39% | 40,72% | 418 / 921 | CRO-001 — Em avaliação | Manter tratamento: acumulado posterior 349/848 vs 755/1885, diferença entre mudanças incerta, volume 20,54% e somente quarta/quinta. Rotação PR #18 não reinicia avaliação. Atualizar mesmo PR documental #16. |
| 2026-10-17 — 09h São Paulo | 2026-10-16, terceiro dia completo pós-publicação | 41,46% | 37,96% | 410 / 1030 | CRO-001 — Em avaliação | Checkpoint exploratório: 519/1258 vs 1146/2915 no pós; diferença entre mudanças +2,78 p.p., IC95% −0,88 a +6,44; 30,47% do volume planejado, somente quarta–sexta. Manter tratamento e PR documental #16; rotações humanas #19/#20 não reiniciam avaliação. |
| 2026-10-18 — 09h São Paulo | 2026-10-17, quarto dia completo pós-publicação | 40,92% | 39,24% | 435 / 971 | CRO-001 — Em avaliação | Manter tratamento: pós697/1693 vs1527/3886, diferença entre mudanças+2,71p.p.,IC95%−0,56 a+5,98;41,01% do volume planejado, quarta–sábado. Orçamento experimental externo100→150/dia às23:40:22 de17/out: preservar baseline e registrar fases de entrega. Mesmo PR documental#16. |

### Série diária retrospectiva — snapshot de 2026-10-13

| Dia no fuso da conta | LPV exp. | Leads exp. | CVR exp. | LPV controle | Leads controle | CVR controle |
|---|---|---|---|---|---|---|
| 2026-09-29 | 314 | 128 | 40,76% | 284 | 141 | 49,65% |
| 2026-09-30 | 246 | 91 | 36,99% | 262 | 108 | 41,22% |
| 2026-10-01 | 268 | 112 | 41,79% | 344 | 138 | 40,12% |
| 2026-10-02 | 407 | 172 | 42,26% | 356 | 135 | 37,92% |
| 2026-10-03 | 309 | 134 | 43,37% | 392 | 133 | 33,93% |
| 2026-10-04 | 410 | 151 | 36,83% | 406 | 157 | 38,67% |
| 2026-10-05 | 464 | 149 | 32,11% | 451 | 162 | 35,92% |
| 2026-10-06 | 426 | 139 | 32,63% | 396 | 141 | 35,61% |
| 2026-10-07 | 326 | 119 | 36,50% | 367 | 137 | 37,33% |
| 2026-10-08 | 424 | 150 | 35,38% | 565 | 207 | 36,64% |
| 2026-10-09 | 383 | 130 | 33,94% | 701 | 289 | 41,23% |
| 2026-10-10 | 447 | 148 | 33,11% | 921 | 332 | 36,05% |
| 2026-10-11 | 430 | 158 | 36,74% | 1080 | 393 | 36,39% |
| 2026-10-12 | 533 | 211 | 39,59% | 1147 | 428 | 37,31% |

## Plano inicial de acompanhamento — superado pela correção e plano do CRO-001 abaixo

1. Ler este arquivo completo na versão mais recente de `main` **e nas branches/PRs de CRO pendentes**. Se o PR de histórico não tiver sido integrado, reutilizar/atualizar esse PR; não criar inicialização duplicada.
2. Confirmar nova publicação e destinos sem os alterar. Separar dados anteriores/posteriores à publicação de 2026-10-13T19:50:46Z; métricas diárias não isolam a hora de publicação. A primeira data inteiramente posterior é 2026-10-14 no fuso da conta; acumular volume e consistência, não impor um número fixo de dias como aprovação.
3. Reconsultar janelas completas e eventuais revisões de atribuição. Só abrir um PR de experimento quando não houver outro pendente e houver referência adequada, registrando CRO-001 com métricas exatas e gates mobile.
4. Obter comprovação verificável do número/prova social antes de qualquer novo uso. Se ela não existir, propor tratamento verdadeiro em mudança separada, sem inventar substitutos.
5. Não atribuir os resultados desta coleta ao histórico novo: documentação não alterou o funil. Nenhum vencedor/perdedor foi declarado.

**PR de acompanhamento (documentação, não experimento):** [#15 — iniciar histórico e diagnóstico ICB](https://github.com/ibombonato/promos-da-lidi/pull/15), aberto para aprovação humana; sem merge ou publicação nesta execução.

## Correção operacional — 2026-10-13

**Esclarecimento do responsável:** os convites do WhatsApp são rotacionados conforme os grupos atingem capacidade, mantendo o mesmo comportamento e conteúdo da landing. Essa rotina não afeta o clique no CTA que define o Lead e não é motivo para adiar um experimento de CRO.

**Verificação técnica:** comparando `87158c2` (2026-09-29) com `origin/main` (`ea788ca`), `index3.html` difere somente nas duas referências ao convite (`href` e `WHATSAPP_GROUP_URL`). Após normalizar esses valores, o HTML inteiro é idêntico. O evento Lead é acionado antes da navegação, no mesmo handler preservado. Não houve mudança de headline, layout, oferta, botão, Pixel ou evento nesse intervalo.

**Correção da interpretação anterior:** as métricas de 29-set a 12-out são uma referência válida do mesmo tratamento visível atual para Lead/LPV, embora os destinos operacionais variem. É desnecessário esperar uma nova janela apenas por rotações de convite. Capacidade/entrada efetiva pertencem à etapa posterior ao clique, separada da métrica proxy; isso não muda a definição de conversão.

**Decisão revista:** implementar agora um único experimento de headline. A diferença incerta versus controle impede declarar um vencedor, mas não impede testar uma hipótese fundamentada. O PR #15, antes exclusivamente documental, será atualizado para conter CRO-001 e seu histórico, evitando um segundo PR/experimento paralelo.

**Regra para execuções futuras:** registrar trocas de convite como manutenção operacional; não tratar como experimento ou reinício de baseline quando o diff confirmar somente destinos e o CTA/evento permanecer igual. Mudanças reais em copy/layout/handler/rastreamento continuam exigindo classificação própria. O agente não está autorizado a trocar os convites por iniciativa própria.

## CRO-001 — Tornar explícita a oferta de perfumes no WhatsApp

**Data de criação:** 2026-10-13

**Data de publicação:** 2026-10-13T23:42:37Z / 2026-10-13 20:42:37 America/Sao_Paulo — timestamp de conclusão do build Pages, confirmado por HTML público HTTP 200 idêntico ao commit publicado.

**Status:** Inconclusivo — avaliação principal encerrada em 2026-10-22 no checkpoint de volume previamente planejado; manter o tratamento publicado sem atribuir vitória ou derrota.

**Branch:** `cro/icb-baseline-2026-10-13`, worktree isolada; reutilizada exclusivamente para este experimento e histórico.

**Pull Request:** [#15 — CRO-001](https://github.com/ibombonato/promos-da-lidi/pull/15), mesclado pelo humano em 2026-10-13T23:42:06Z. A publicação ocorreu pelo fluxo Pages existente após essa aprovação; o agente não realizou merge, auto-merge ou deploy.

**Commit de publicação:** `1a377ea858b18189d7b40b1fd63990376e777712`.

**Screenshot mobile:** [390×844](cro/screenshots/CRO-001-mobile.png) e [360×800](cro/screenshots/CRO-001-mobile-360x800.png), renderizados em Chromium real e inspecionados.

### Problema e hipótese

O headline genérico “Nunca mais / Perca uma promoção!” não identifica o produto nem o canal. Os anúncios ativos citam perfumes, Natura e O Boticário; o visitante precisa ler o parágrafo posterior para reconhecer a oferta. **Explicitar “Perfumes em oferta / No seu WhatsApp” no mesmo bloco deve reduzir o esforço de compreensão e melhorar a correspondência anúncio–landing, aumentando a propensão ao clique por LPV.**

### Evidências e confiança

- Anúncios reais ativos prometem “Perfumes da Natura e O Boticário com preço baixo e cupom de desconto” e “Promos de perfumes e produtos de beleza...”; a nova copy explicita apenas fatos já presentes na oferta, sem criar desconto, número, exclusividade ou depoimento.
- Baseline operacional recente: CVR de 36,98% em 5387 LPV/1992 Leads nos 14 dias e 35,53% em 2969 LPV/1055 Leads nos 7 dias. Há volume para formular e acompanhar um teste; a falta de superioridade estatística hoje não invalida a hipótese de melhoria.
- Screenshots da versão atual demonstram headline genérico e CTA já visível. Não há heatmap, pesquisa de usuários ou teste prévio que prove abandono causado pela headline; o ganho permanece uma hipótese.
- ICE: impacto 7, confiança 5, facilidade 9 (priorização qualitativa, não previsão de lift).

### Alteração realizada — uma variável principal

Somente os dois textos do bloco de headline em `index3.html`:

| Elemento | Antes | Implementado na branch |
|---|---|---|
| `h1` | Nunca mais | Perfumes em oferta |
| `h2` | Perca uma promoção! | No seu WhatsApp |

CSS, parágrafo de oferta, prova social existente, benefícios, CTA, recursos, convites, parâmetros, Pixel/eventos e JavaScript foram preservados byte a byte. O contraste do CTA não foi alterado neste experimento. A quebra natural da nova headline foi validada mobile, sem modificar tipografia, espaçamento ou posição do botão como segunda hipótese; seu fluxo vertical muda apenas pela altura natural do texto.

### QA da implementação

- Guard de substituição exata aprovado: `index3.html` difere de `origin/main` exclusivamente nos dois textos `h1`/`h2`; CSS, todos os scripts, CTA completo, href/src e `index4_li.html` idênticos ao baseline. Nenhum recurso ou dependência de execução novo.
- Teste RED do novo headline falhou antes da alteração, conforme esperado; depois da implementação passou. Script real do CTA executado em Node VM: 11 verificações aprovadas, sem rede/entrada no WhatsApp.
- Chromium real na prévia HTTP local: screenshots exatos 390×844 e 360×800 inspecionados visualmente, sem overflow horizontal ou cortes de headline/CTA. CTA inteiro na primeira dobra: 390×844 y 503,75–565,75, altura 62 px; 360×800 y 500,141–560,141, altura 60 px.
- Rolagem em 360×800 até o fim, grid de seis benefícios e foto íntegros. Viewports adicionais 320×740 e desktop 1280×900 sem overflow; sem exceções JavaScript observadas. Não equivale a Safari real ou Web Vitals de campo.
- Clique físico no CTA no Chromium validou uma chamada local interceptada `['track', 'Lead']` e timer de 150 ms. Pixel/WhatsApp bloqueados antes da navegação e timer interceptado apenas no ambiente QA; URL ficou na prévia local. Nenhum evento real de Meta nem entrada no grupo foi disparado. A interceptação não está no código da landing/PR.

![CRO-001 — screenshot mobile 390×844](cro/screenshots/CRO-001-mobile.png)

### Métricas anteriores — snapshot real desta execução

**Período principal de referência congelado após confirmação da publicação:** 2026-09-29 a 2026-10-12, os 14 dias completos anteriores ao dia de publicação, em America/Sao_Paulo. Os valores abaixo são o snapshot da coleta de 2026-10-13; revisões de atribuição posteriores deverão ser registradas como revisões, sem apagar esse snapshot.

| Métrica | Experimental | Controle |
|---|---|---|
| Landing Page Views | 5387 | 7672 |
| Leads atribuídos (proxy clique) | 1992 | 2901 |
| CVR | 36,98% | 37,81% |
| Investimento | R$ 1162,06 | R$ 1568,22 |
| CPL proxy | R$ 0,58 | R$ 0,54 |

**Sensibilidade recente:** 2026-10-06 a 2026-10-12: experimental 1055/2969 = 35,53%, controle 1927/5177 = 37,22%. As janelas de 1/3 dias e série diária permanecem no diagnóstico acima; não escolher retrospectivamente apenas a janela mais favorável.

### Métricas posteriores

**Período principal de encerramento:** 2026-10-14 a 2026-10-21, oito dias completos; snapshot consultado em 2026-10-22. Baseline congelado 29/set–12/out reconsultado sem revisão; excluir 13/out parcialmente exposto. Snapshots anteriores preservados integralmente nos acompanhamentos datados. Mudança externa de orçamento em 17/out às23:40:22 São Paulo: manter baseline/acumulado e diagnósticos separados para 14–16/out, transição17/out e 18–21/out. Dois anúncios externos começaram a entregar no fim de 21/out, com apenas 4 LPV/3 Leads no acumulado; manter desfecho principal e mostrar sensibilidades, não substituir janela retrospectivamente.

| Métrica | Experimental | Controle |
|---|---|---|
| Landing Page Views | 4346 | 7627 |
| Leads atribuídos (proxy clique) | 1676 | 2966 |
| CVR | 38,56% | 38,89% |
| Investimento | R$ 996,59 | R$ 1546,46 |
| CPL proxy | R$ 0,59 | R$ 0,52 |

**Variação observada pós−pré em p.p.:** Experimental +1,59; controle +1,08. IC95% nominal aproximado experimental −0,35 a +3,52 p.p., sem ajuste sequencial. Diferença entre mudanças +0,51 p.p., IC95% −1,97 a +2,99 p.p.; não é impacto causal comprovado.

**Variação relativa observada:** Experimental +4,29%; controle +2,84%; diferença entre evoluções relativas +1,45 pontos percentuais, descritiva. CPL experimental +1,93%, controle −3,55% sobre valores não arredondados.

**Conclusão final em 2026-10-22:** **Inconclusivo; encerrar a avaliação principal**, sem prolongá-la em busca de significância. Volume4346LPV (105,28% da referência4128), oito dias completos e cobertura de todos os dias da semana. Diferença entre mudanças e antes/depois experimental incluem zero, com sinais inconsistentes entre fases de orçamento. O MDE de planejamento +3p.p. não foi demonstrado; ausência de evidência não prova equivalência ou ausência de efeito. Excluindo somente os novos anúncios externos:1673/4342=38,53%, diferença entre mudanças+0,48p.p.,IC95%−2,00 a+2,95; sensibilidade14–20/out:+0,43p.p.,IC95%−2,13 a+2,99. Preservar resultado principal14–21/out, baseline e snapshots. Manter headline por continuidade, não porque venceu; sem suporte para reversão. Monitoramento futuro não reabre silenciosamente CRO-001. Nenhum HTML/Meta alterado pelo agente.

**Aprendizado da avaliação:** explicitar oferta/canal era uma hipótese fundamentada, mas os dados observacionais não demonstraram ganho atribuível à headline. Mudança externa de orçamento e de mix limita isolamento. O próximo teste deve manter uma variável principal e registrar composição do tráfego/baseline antes da implementação; não reutilizar4128LPV como limiar universal.

**Aprendizado já confirmado:** rotações de convite não são modificações do tratamento visível nem reset do baseline de clique.

### Resultado esperado e plano de avaliação pré-definido

1. **Métrica principal:** Lead atribuído/LPV, definição inalterada; CPL proxy secundário. Objetivo de planejamento: detectar aproximadamente **+3 p.p.**, não promessa de resultado. Não medir sucesso por quantidade de commits ou por um dia favorável.
2. Confirmar commit de publicação e HTML real antes de começar o período posterior. Quando a publicação ocorrer, congelar a referência dos **14 dias completos imediatamente anteriores** à publicação, aplicando a mesma regra ao controle; se o merge demorar, atualizar esse baseline sem escolher o período pelo resultado. As métricas acima são o snapshot de planejamento disponível hoje.
3. Excluir o dia de publicação parcialmente exposto ao tratamento da comparação diária principal. Acumular amostra posterior e cobertura de dias da semana/variação de tráfego; mudanças operacionais de convite não reiniciam essa contagem se o tratamento/evento permanecer igual.
4. Aproximação de planejamento para duas proporções independentes, CVR inicial 36,98%, MDE +3 p.p., alfa bilateral 5%, poder 80%: **4128 LPV por período**. É uma referência de volume calculada, não garantia de poder em dados atribuídos/dependentes nem critério único de término. Não avaliar como vencedor/perdedor antes de volume e cobertura adequados apenas por oscilações diárias; verificar intervalos, consistência e contexto do controle.
5. Calcular diferenças absolutas/relativas antes/depois, IC95% e evolução do controle em períodos comparáveis; inspecionar mix de criativos/dispositivos/posicionamentos e revisões de atribuição. Campanhas distintas e antes/depois não randomizados limitam causalidade mesmo com intervalos favoráveis. Resultado positivo sem suporte suficiente fica Inconclusivo.
6. Manter CRO-001 como único experimento pendente/em avaliação. Regressão funcional grave exige comunicar/propor correção/reversão por PR, nunca merge/deploy/reversão automática.

### Diário — revisão da decisão na mesma data

| Execução | Referência | CVR exp. / controle | LPV exp. / controle | Experimento | Decisão |
|---|---|---|---|---|---|
| 2026-10-13 — após esclarecimento operacional | 29-set a 12-out; snapshot da mesma coleta | 36,98% / 37,81% | 5387 / 7672 | CRO-001 — Em PR | Headline implementada e QA aprovado; aguardar aprovação/publicação humana e avaliar dados posteriores ao experimento, não às rotações de convite. |

## Acompanhamento pós-merge — 2026-10-13

**Evidências de publicação:** PR #15 MERGED em 23:42:06Z; Pages build `1a377ea858b18189d7b40b1fd63990376e777712` com status `built`, iniciado 23:42:08Z e concluído 23:42:37Z; HTML público de `index3.html` HTTP 200, byte a byte idêntico a `origin/main`, com “Perfumes em oferta / No seu WhatsApp”. Publicação foi confirmada separadamente do merge. Nenhuma alteração de código nesta atualização de acompanhamento.

| Execução | Referência | CVR exp. / controle | LPV exp. / controle | Experimento | Decisão |
|---|---|---|---|---|---|
| 2026-10-13 — confirmação pós-merge | Baseline 29-set–12-out; pós-CRO-001 ainda sem dia completo | Baseline 36,98% / 37,81%; pós pendente | Baseline 5387 / 7672; pós pendente | CRO-001 — Em avaliação | Confirmar publicação, congelar período anterior e acompanhar diariamente. Não implementar outro experimento durante essa avaliação. |

### Rotina diária configurada e verificada

- Job do perfil `rich-conversion`: `714c96de5c45`, nome “ICB CRO diário — acompanhamento às 09h São Paulo”.
- Cron `0 12 * * *` em UTC, equivalente a **09h America/Sao_Paulo** na configuração atual. Agendamento ativo, repetição diária indefinida, continuidade habilitada, sem pin de modelo. Scheduler confirmado ativo por `hermes -p rich-conversion cron status`.
- Próxima execução: **2026-10-14T12:00:00Z / 14-out às 09h São Paulo**. Esse primeiro acompanhamento valida estado/baseline e diagnóstico; ainda não haverá um dia inteiro posterior ao experimento.
- **15-out às 09h:** primeira leitura de um dia inteiro do CRO-001 (14-out).
- **17-out às 09h:** checkpoint exploratório com três dias completos (14–16-out), sem classificar vencedor ou interromper apenas por oscilação.
- Depois, acompanhamento diário de CVR/CPL/LPV/volume/controle e backlog. Planejar futuras hipóteses em paralelo é permitido; publicar/implementar tratamentos simultâneos não é.
- Entrega do agendamento: **local**, com relatório salvo pelo scheduler em `/home/ibombonatohermes/.hermes/profiles/rich-conversion/cron/output/714c96de5c45/`; não existe promessa de notificação automática nesta conversa TUI. O agente também mantém este histórico por PR, reutilizando um PR de acompanhamento pendente em vez de criar duplicatas.

### Previsão de volume, não prazo de conclusão

Com o tráfego do snapshot recente, experimental tem média de 424,14 LPV/dia na janela de 7 dias e 384,79 na janela de 14 dias. Para acumular a referência aproximada de 4128 LPV posteriores seriam **10–11 dias completos**, se esse ritmo se mantiver: primeira revisão matinal com esse volume estimado em **24–25/out**. Isso é projeção, não data obrigatória para concluir ou lançar CRO-002. A decisão depende de volume real, incerteza, consistência, cobertura semanal e fatores externos; sem suporte suficiente, resultado Inconclusivo.

### Materiais para próximos experimentos

Nenhum material extra é necessário para medir CRO-001 ou preparar a hipótese de contraste do CTA. Para futuras mudanças de confiança/demonstração de valor, solicitar apenas materiais reais: exemplos recentes de ofertas/cupons com loja/data/preço verificáveis; screenshot do conteúdo do grupo com nomes/telefones ocultos; depoimentos autorizados; comprovação da afirmação existente “Mais de 16.000” ou número atual verificável sem inflar por duplicidade de participantes. Nenhum material será inventado ou usado como prova social validada sem evidência.

## Acompanhamento diário — 2026-10-14

**Execução:** iniciada às 09h America/Sao_Paulo; consolidação dos dados em 2026-10-14T12:06:18Z. Histórico integral de `origin/main` e do PR documental #16 consultado antes do diagnóstico; PRs abertos/fechados e commits recentes inspecionados. O único PR aberto é [#16 — acompanhamento CRO-001](https://github.com/ibombonato/promos-da-lidi/pull/16), exclusivamente `CRO_EXPERIMENTS.md`; reutilizado nesta execução, sem novo PR de experimento. Worktree própria criada a partir de `origin/main`, incorporando o histórico pendente sem modificar worktrees existentes.

**Publicação reconfirmada:** PR #15 mesclado pelo humano; Pages `built` para `1a377ea858b18189d7b40b1fd63990376e777712`, conclusão do build **2026-10-13T23:42:37Z / 20:42:37 São Paulo**. Em 2026-10-14T12:06:18Z, HTML público de ambas as landings HTTP 200 idêntico byte a byte ao commit publicado. A experimental contém “Perfumes em oferta / No seu WhatsApp”; sua comparação com o pré-tratamento difere somente nos dois textos do headline. CTA, scripts, Pixel/eventos e destinos intactos, com `href` igual à constante de navegação. Nenhuma alteração de publicação posterior encontrada. Timestamp de build é evidência do sistema de publicação, não instante exato de troca para cada visitante.

### Dados atuais — diagnóstico de campanhas, não resultado do headline

MCP oficial Meta Ads via transporte ad hoc: sessão inicializada, protocolo negociado `2025-06-18`, conta confirmada consultável/habilitada, campos verificados e somente chamadas de leitura. Totais de investimento, impressões, cliques, LPV e Leads das quatro janelas e do baseline conciliados com a série diária Graph GET. Aliases selecionados, não somados; atribuição unificada preservada. Paginação inspecionada, sem páginas seguintes ou continuação pendente nas consultas de métricas.

**Último dia completo:** 2026-10-13; **14-out está em andamento e não foi incluído**. Todas as janelas abaixo incluem o dia de publicação parcialmente exposto: servem ao diagnóstico geral e **não** ao efeito puro do CRO-001.

| Janela | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 dia | 2026-10-13 a 2026-10-13 | Experimental | R$ 92,03 | 22659 | 544 | 459 | 176 | 38,34% | R$ 0,52 |
| 1 dia | 2026-10-13 a 2026-10-13 | Controle | R$ 183,18 | 53317 | 1185 | 990 | 365 | 36,87% | R$ 0,50 |
| 3 dias | 2026-10-11 a 2026-10-13 | Experimental | R$ 314,92 | 72692 | 1690 | 1422 | 545 | 38,33% | R$ 0,58 |
| 3 dias | 2026-10-11 a 2026-10-13 | Controle | R$ 634,29 | 174780 | 3835 | 3217 | 1186 | 36,87% | R$ 0,53 |
| 7 dias | 2026-10-07 a 2026-10-13 | Experimental | R$ 669,51 | 153750 | 3569 | 3002 | 1092 | 36,38% | R$ 0,61 |
| 7 dias | 2026-10-07 a 2026-10-13 | Controle | R$ 1160,96 | 310435 | 6874 | 5771 | 2151 | 37,27% | R$ 0,54 |
| 14 dias | 2026-09-30 a 2026-10-13 | Experimental | R$ 1188,61 | 267983 | 6533 | 5532 | 2040 | 36,88% | R$ 0,58 |
| 14 dias | 2026-09-30 a 2026-10-13 | Controle | R$ 1690,81 | 427889 | 9854 | 8378 | 3125 | 37,30% | R$ 0,54 |

**Baseline principal congelado — 29-set a 12-out:** reconsultado hoje, sem revisão nos totais de LPV, Leads ou investimento: experimental **1992/5387 = 36,98%**, IC95% Wilson **35,70%–38,28%**, CPL R$ 0,58; controle **2901/7672 = 37,81%**, IC95% **36,73%–38,90%**, CPL R$ 0,54. Snapshot anterior preservado. A referência histórica informada de 36% continua sem denominador; nenhum teste de significância contra ela.

**Pós-publicação principal:** primeiro dia elegível é **14-out**, ainda incompleto nesta leitura. LPV/Leads/CVR/CPL posteriores permanecem **pendentes, não zero**. Excluir 13-out da análise principal. Não há estimativa de lift do CRO-001, nem classificação vencedor/perdedor.

### Diagnóstico, incerteza e mix

- CVR 7d experimental **36,38%**, IC95% Wilson **34,67%–38,11%**; controle **37,27%**, IC95% **36,03%–38,53%**. Diferença experimental−controle **−0,90 p.p.**, IC95% normal aproximado **−3,02 a +1,23 p.p.**: comparação incerta/observacional, não efeito do headline. Experimental versus referência histórica36: **+0,38 p.p. / +1,04% relativo**, somente descritivo.
- Semanas não sobrepostas **30-set–6-out → 7–13-out**: experimental **948/2530 = 37,47% → 1092/3002 = 36,38%**, **−1,09 p.p. / −2,92% relativo**; controle **974/2607 = 37,36% → 2151/5771 = 37,27%**, **−0,09 p.p. / −0,24% relativo**. Diferença entre evoluções relativas **−2,68 pontos percentuais de variação relativa**, entre mudanças absolutas **−1,01 p.p.**; não atribuir à publicação noturna de 13-out nem usar como causalidade.
- Campanhas e conjuntos continuam ACTIVE. Experimental mantém dois anúncios efetivamente ativos: `120251541120490505` (**935 Leads / 2566 LPV**, CVR 36,44%, R$ 579,02) e `120250848857170505` (**157/436**, CVR 36,01%, R$ 90,49); criativo antigo permanece PAUSED. Controle tem `120250926403940505` ativo apesar do nome “PAUSADO”. Copy/destinos atuais permanecem alinhados às páginas corretas; nenhum timestamp novo de edição nesses anúncios/conjuntos em relação ao diagnóstico anterior. Timestamp sozinho não prova ausência de todo fator externo.
- Pixel `1504398471438133`; atribuição dos dois conjuntos continua clique7d/visualização1d/vídeo-engajado1d. Lead no script é proxy pré-redirecionamento, não confirmação de participante. Compartilhar Pixel/atribuição não fornece coortes deduplicadas.
- LPV/clique 7d: **84,11% / 83,95%**; sem discrepância grosseira exclusiva da experimental. Dispositivos: Android smartphone **766/1993 = 38,43% / 1452/3641 = 39,88%**; iPhone **325/1007 = 32,27% / 697/2122 = 32,85%**. A menor taxa de iPhone nas duas campanhas não comprova falha de Safari.
- Posicionamentos Instagram 7d: Stories **909/2563 = 35,47% / 1841/5106 = 36,06%**; feed **150/344 = 43,60% / 202/432 = 46,76%**; Reels **33/95 = 34,74% / 107/229 = 46,72%**. Mix e amostras diferentes limitam comparabilidade; preservar segmentação/Meta em leitura.

### Decisão e próxima observação

**Decisão:** manter CRO-001 **Em avaliação**, sem mudança em `index3.html` ou controle. Gate concreto faltante: um dia pós-publicação completo, seguido de volume/consistência suficientes. A primeira coleta elegível ocorre em **15-out**, incluindo 14-out; isso inicia medição, não encerra avaliação. Checkpoint exploratório de três dias completos em 17-out, sem parada por primeiro p-valor favorável.

Plano original mantido: MDE +3 p.p., alfa bilateral 5%, poder80%, referência aproximada **4128 LPV/período**, sob hipóteses binomiais. Hoje, médias experimentais de **428,86 LPV/dia (7d)** e **395,14 (14d)** projetam **10–11 dias completos** para esse volume pós-tratamento, com primeiras consultas matinais estimadas em **24–25/out** se o ritmo persistir. Não é garantia de poder, data de vitória nem único critério; conferir IC95%, cobertura semanal, consistência, atribuição e mix. As datas são observações planejadas, não configuração nova de agenda.

Backlog preservado: contraste do CTA como teste separado, não implementado enquanto CRO-001 é avaliado. Não depende de material extra. Provas sociais/depoimentos/prints/ofertas exigem evidência real, autorização e anonimização quando aplicável; sem invenção ou ampliação da afirmação existente não comprovada.

**Escopo desta execução:** somente documentação no PR #16; nenhum merge, auto-merge, deploy, alteração Meta, rastreamento, convite ou mensagem externa. QA mobile de implementação não foi repetida hoje porque não houve alteração de HTML/CSS/scripts; o HTML atual foi reconfirmado idêntico ao já validado em 390×844 e 360×800. Isso não equivale a novo teste de Safari real ou performance de campo.

**Artefatos locais sem secrets:** `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-14/`: `analysis.json`, `daily-graph.json` (série diária completa 29-set–13-out com investimento/impressões/cliques/LPV/Leads), respostas MCP atuais, `traffic-audit.json`, `live-validation.json`, `report.md` e verificação remota do PR. Nenhum snapshot antigo foi utilizado como substituto dos dados atuais.

## Acompanhamento diário — 2026-10-15

**Execução:** iniciada às 09h America/Sao_Paulo; consolidação em 2026-10-15T12:03:41Z. Histórico integral de origin/main e do PR #16, PRs abertos/fechados e commits consultados antes do diagnóstico. Worktree nova a partir de origin/main (`b72e3ce`), incorporando histórico pendente sem alterar worktrees existentes. Único PR aberto: #16, exclusivamente documental; reutilizado, sem novo experimento.

**Publicação e manutenção operacional:** build inicial do CRO-001 reconfirmado pela API Pages: `1a377ea858b18189d7b40b1fd63990376e777712`, concluído em 2026-10-13T23:42:37Z / 20:42:37 São Paulo. Humano mesclou [PR #17](https://github.com/ibombonato/promos-da-lidi/pull/17) em 2026-10-15T03:26:29Z; diff contém somente as duas referências do convite em index3.html. Pages atual `b72e3cea4605dc35b287772cc0d592e49a53241a`, build `built` concluído em 2026-10-15T03:27:07Z / 00:27:07 São Paulo. Às 12:02:13Z, ambas as páginas públicas HTTP200 e byte a byte iguais ao commit. Experimental normalizada apenas nos convites é idêntica ao tratamento inicial; controle intacto. href/constante coerentes; headline, CSS, CTA, Pixel/evento/handler preservados; Lead continua antes da navegação. **Rotação não reinicia CRO-001 nem baseline.** Build é evidência do sistema, não instante exato para cada visitante.

### Dados atuais e conciliação

MCP oficial ad hoc: sessão inicializada, protocolo2025-06-18, schemas/conta consultável e campos verificados; somente ferramentas de leitura. Totais das quatro janelas e baseline conciliados com série diária Graph GET, aliases selecionados, atribuição unificada preservada e paginação/continuações inspecionadas. Breakdowns7d/pós conciliados em contagens; dispositivo experimental7d soma R$700,609999 versus total R$700,61, microarredondamento inferior a um centavo, sem divergência nos totais principais. 15/out parcial excluído.

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-14 a 2026-10-14 | Experimental | R$ 96,37 | 22577 | 535 | 430 | 176 | 40,93% | R$ 0,55 |
| 1 | 2026-10-14 a 2026-10-14 | Controle | R$ 191,78 | 49723 | 1153 | 964 | 380 | 39,42% | R$ 0,50 |
| 3 | 2026-10-12 a 2026-10-14 | Experimental | R$ 297,60 | 71555 | 1704 | 1422 | 563 | 39,59% | R$ 0,53 |
| 3 | 2026-10-12 a 2026-10-14 | Controle | R$ 592,57 | 166985 | 3698 | 3101 | 1173 | 37,83% | R$ 0,51 |
| 7 | 2026-10-08 a 2026-10-14 | Experimental | R$ 700,61 | 159845 | 3733 | 3106 | 1149 | 36,99% | R$ 0,61 |
| 7 | 2026-10-08 a 2026-10-14 | Controle | R$ 1282,41 | 340699 | 7580 | 6368 | 2394 | 37,59% | R$ 0,54 |
| 14 | 2026-10-01 a 2026-10-14 | Experimental | R$ 1224,53 | 281997 | 6787 | 5716 | 2125 | 37,18% | R$ 0,58 |
| 14 | 2026-10-01 a 2026-10-14 | Controle | R$ 1815,34 | 467838 | 10695 | 9080 | 3397 | 37,41% | R$ 0,53 |

Janelas3/7/14d misturam tratamentos e servem ao diagnóstico geral, **não** ao efeito puro do headline. Período principal posterior: somente14/out; 13/out misto permanece excluído. Lead é proxy pré-redirecionamento, não entrada confirmada.

### CRO-001 — primeiro dia posterior completo

**Status Em avaliação; resultado inicial inconclusivo.** Baseline29/set–12/out reconsultado sem revisão de LPV/Leads/investimento: experimental1992/5387=36,98%, controle2901/7672=37,81%. Snapshot original preservado. Referência histórica36 sem denominador apenas descritiva.

- Posterior14/out: experimental176/430=40,93%, IC95% Wilson36,38%–45,64%, CPL R$0,55; controle380/964=39,42%, IC95%36,38%–42,54%, CPL R$0,50.
- Variação experimental pós−pré **+3,95p.p. / +10,69% relativo**, IC95% normal aproximado da diferença **−0,87 a +8,78p.p.**, inclui zero. Controle também subiu: **+1,61p.p. / +4,25%**, IC95% da diferença−1,66 a +4,88p.p.
- Diferença entre mudanças absolutas **+2,35p.p.**; entre evoluções relativas **+6,44 pontos percentuais de variação relativa**. Diferença experimental−controle posterior+1,51p.p., IC95%−4,07 a +7,09p.p. Comparações observacionais, não impacto causal; não há randomização, visitantes únicos ou equivalência de tráfego garantidas. Intervalos binomiais são aproximações para eventos atribuídos potencialmente dependentes.
- Somente430 LPV posteriores = **10,42%** da referência de planejamento4128, cobertura de apenas uma quarta-feira. Resultado favorável insuficiente para vencedor/perdedor, interrupção ou tratamento simultâneo.

### Mix, evolução e revisões

- Campanhas/conjuntos ACTIVE. Dois anúncios experimentais ativos (`120251541120490505`, produtos atualizados; `120250848857170505`, texto4em1), antigo pausado; controle `120250926403940505` ativo apesar do nome. Todas as bodies/titles e destinos reconferidos; anúncio→index3/index4_li corretos. Timestamps de anúncios/conjuntos inalterados desde diagnóstico anterior. Pixel1504398471438133, atribuição clique7d/visualização1d/vídeo-engajado1d em ambos.
- Em14/out, produtos atualizados158/374 LPV, CVR42,25%, R$84,31; texto4em1 18/56,32,14%,R$12,06. Distribuição desigual/não randomizada, não declarar vencedor entre criativos.
- Dispositivos14/out: Android smartphone exp.110/267=41,20% / controle228/542=42,07%; iPhone66/163=40,49% /150/419=35,80%. Não inferir defeito de Safari. Stories experimental157/376=41,76%; feed14/45=31,11%; Reels5/9=55,56%, amostras muito pequenas nos últimos dois.
- LPV/clique14/out **80,37% /83,61%**, 7d **83,20% /84,01%**. Acompanhar persistência/mix antes de atribuir defeito de carregamento ao headline; não houve medição de performance de campo.
- Semanas não sobrepostas1–7/out→8–14/out: experimental976/2610=37,39%→1149/3106=36,99% (**−0,40p.p./−1,07% relativo**); controle1003/2712=36,98%→2394/6368=37,59% (**+0,61p.p./+1,65%**). Diferença entre evoluções relativas−2,72 pontos percentuais; entre mudanças absolutas−1,01p.p. Descritivo; não atribuir uma semana quase toda anterior ao novo headline. Diferença7d experimental−controle−0,60p.p., IC95%−2,67 a +1,47p.p.
- Revisão versus snapshot14/out: controle13/out investimento R$183,18→183,19 e impressões53317→53319; LPV990/Leads365 inalterados. Registro anterior preservado; nenhuma revisão no baseline congelado.

### Decisão e próxima observação

Manter CRO-001 **Em avaliação**, sem alteração de landing. Próxima coleta inclui15/out completo; checkpoint exploratório14–16/out em17/out. Gate faltante: volume/cobertura semanal/consistência e avaliação de incerteza/mix/atribuição, não confirmação de publicação nem uma nova janela após convite.

Plano original mantido: MDE+3p.p., alfa bilateral5%, poder80%, referência binomial aproximada4128 LPV/período, não garantia nem único critério. Restam3698 LPV; médias443,71LPV/dia(7d) e408,29(14d) projetam mais9–10 dias completos, com consultas matinais estimadas24–25/out se tráfego se mantiver. Não encerrar por oscilação ou primeiro p-valor favorável; avaliar explicitamente o experimento antes do seguinte.

Backlog: contraste do CTA em teste separado após avaliar CRO-001; nenhum material extra necessário. Futuras provas sociais somente reais/verificáveis/autorizadas/anonimizadas. Sem alteração deHTML/CSS/scripts: QA visual mobile não repetida hoje; equivalência ao tratamento já validado390×844/360×800 reconfirmada após normalizar apenasURLs. Não equivale a Safari real ou performance de campo.

**Escopo:** somente CRO_EXPERIMENTS.md no mesmo PR#16; sem alteração de Meta, landings, rastreamento ou convites pelo agente, sem merge dePR/auto-merge/deploy ou mensagens externas. Artefatos atuais sem tokens em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-15/`: analysis.json, série diáriaGraph29/set–14/out, respostasMCP, audits7d/pós, validaçãoPages/live, revisão dos snapshots, report.md e remote-verification.json. Helpers reaproveitados como código; dados atuais reconsultados, nunca substituídos por snapshots antigos.

## Acompanhamento diário — 2026-10-16

**Execução:** 09h America/Sao_Paulo; métricas consolidadas em 2026-10-16T12:02:34Z. Histórico integral da main atual e do PR #16, PRs abertos/fechados e commits consultados antes do diagnóstico. Worktree nova a partir de origin/main `c18637f`, incorporando o histórico pendente; outras worktrees preservadas. Único PR aberto: [#16](https://github.com/ibombonato/promos-da-lidi/pull/16), documental, reutilizado sem novo experimento.

**Publicação:** build inicial do CRO-001 `1a377ea858b18189d7b40b1fd63990376e777712`, conclusão 2026-10-13T23:42:37Z (20:42:37 São Paulo), reconfirmado pela API Pages. [PR #18](https://github.com/ibombonato/promos-da-lidi/pull/18) mesclado pelo humano em 2026-10-16T01:59:53Z: somente href e WHATSAPP_GROUP_URL em index3.html. Pages atual `c18637ff3daf6cad3e97d7738e9fac10323a7e86`, built em 2026-10-16T02:00:30Z (15/out 23:00:30 São Paulo). HTML de ambas as páginas público HTTP200 e byte a byte igual ao commit às 12:01:33Z. Normalizando somente convites, experimental inteira idêntica ao tratamento inicial; controle intacto. Headline, CSS, CTA, Pixel/evento/handler preservados, href/constante coerentes, Lead pré-redirecionamento. **Manutenção operacional, não novo experimento nem reinício do baseline.** Build não é instante exato de exposição por visitante.

### Métricas atuais — dias completos

MCP oficial ad hoc inicializado, protocolo negociado **2025-11-25** reutilizado; schemas/conta consultável/campos confirmados, somente ferramentas de leitura. Quatro janelas e baseline conciliados exatamente em investimento/impressões/cliques/LPV/Leads com série diária Graph GET; aliases selecionados, não somados; atribuição unificada preservada. Paginação/continuações inspecionadas. Breakdowns de baseline/7d/pós conciliados em contagens; gasto por dispositivo do controle pós soma R$373,920001 versus R$373,92, resíduo −R$0,000001, inferior a um centavo, sem divergência nos totais principais. Excluir 16/out parcial.

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-15 a 2026-10-15 | Experimental | R$ 92,07 | 21223 | 500 | 418 | 173 | 41,39% | R$ 0,53 |
| 1 | 2026-10-15 a 2026-10-15 | Controle | R$ 182,13 | 45340 | 1078 | 921 | 375 | 40,72% | R$ 0,49 |
| 3 | 2026-10-13 a 2026-10-15 | Experimental | R$ 280,47 | 66459 | 1579 | 1307 | 525 | 40,17% | R$ 0,53 |
| 3 | 2026-10-13 a 2026-10-15 | Controle | R$ 557,11 | 148385 | 3416 | 2875 | 1120 | 38,96% | R$ 0,50 |
| 7 | 2026-10-09 a 2026-10-15 | Experimental | R$ 699,28 | 158730 | 3703 | 3100 | 1172 | 37,81% | R$ 0,60 |
| 7 | 2026-10-09 a 2026-10-15 | Controle | R$ 1351,67 | 356337 | 7984 | 6724 | 2562 | 38,10% | R$ 0,53 |
| 14 | 2026-10-02 a 2026-10-15 | Experimental | R$ 1238,87 | 291836 | 6974 | 5866 | 2186 | 37,27% | R$ 0,57 |
| 14 | 2026-10-02 a 2026-10-15 | Controle | R$ 1916,46 | 501178 | 11378 | 9657 | 3634 | 37,63% | R$ 0,53 |

Janelas3/7/14d misturam tratamentos; diagnóstico geral, não efeito puro do headline. Lead é **proxy de clique antes da navegação, não entrada confirmada no grupo**. Baseline histórico informado36% sem denominador: referência descritiva, não teste estatístico.

### CRO-001 — dois dias completos posteriores (14–15/out)

**Status Em avaliação; resultado ainda inconclusivo.** Baseline congelado29/set–12/out reconsultado sem revisão dos totais: experimental1992/5387=36,98%, controle2901/7672=37,81%; snapshot original preservado. 13/out parcialmente exposto continua excluído.

| Métrica posterior | Experimental | Controle |
|---|---:|---:|
| Investimento | R$ 188,44 | R$ 373,92 |
| Impressões | 43800 | 95066 |
| Cliques no link | 1035 | 2231 |
| LPV | 848 | 1885 |
| Leads proxy | 349 | 755 |
| CVR | 41,16% | 40,05% |
| CPL proxy | R$ 0,54 | R$ 0,50 |

- Experimental pós−pré **+4,18p.p./+11,30% relativo**, IC95% normal nominal **+0,62 a +7,73p.p.**; CVR pós Wilson95%37,89%–44,50%. O intervalo nominal passou a excluir zero, mas **não é ajustado para leituras sequenciais** nem justifica vitória/parada precoce. Controle também melhorou **+2,24p.p./+5,92%**, IC95% diferença−0,22 a+4,70p.p.; CVR pós Wilson37,86%–42,28%.
- Diferença entre mudanças absolutas **+1,94p.p.**, IC95% aproximado **−2,39 a+6,26p.p.**, inclui zero. Entre evoluções relativas **+5,37 pontos percentuais de variação relativa**. Diferença experimental−controle no pós **+1,10p.p.**, IC95%−2,88 a+5,09p.p. Descrições observacionais; quatro proporções tratadas como independentes são aproximação, não causalidade randomizada nem coorte deduplicada.
- Somente **848 LPV posteriores =20,54%** da referência planejada4128, com cobertura de quarta/quinta. Há sinal favorável antes/depois, mas faltam volume/cobertura/consistência e separação de fatores externos; preservar avaliação, sem tratamento simultâneo.

### Tráfego, evolução e revisões

- Campanhas/conjuntos ACTIVE; dois anúncios experimentais ativos (`120251541120490505`, produtos atualizados; `120250848857170505`, texto4em1), antigo pausado; controle `120250926403940505` ativo apesar do nome. Campos atuais dos anúncios ativos/conjuntos, copy completa, destinos e atribuição idênticos à consulta anterior. Única diferença na resposta do anúncio antigo pausado foi URL assinada de miniatura, não mudança de criativo/entrega. Pixel1504398471438133, atribuição clique7d/visualização1d/vídeo-engajado1d preservados.
- **Mix não constante:** participação do anúncio produtos atualizados nos LPV experimentais **81,77% no pré →90,68% no pós**. CVR desse anúncio37,41%→41,87%; texto4em135,03%→34,18%, este com apenas79LPV posteriores. Não atribuir ao headline toda a mudança agregada nem declarar vencedor entre criativos.
- Android experimental39,77% (1359/3417)→41,56% (219/527); iPhone32,11% (632/1968)→40,50% (130/321). Controle Android40,47%→42,16%, iPhone33,91%→37,16%. Share de LPV Android exp.63,43%→62,15%, controle59,38%→56,87%. Não diagnosticar defeito Safari por esses dados. Stories exp. share88,58%→88,56%, CVR35,85%→41,41%; controle88,56%→87,90%, CVR36,87%→39,05%. Feed/Reels pós experimentais74/23LPV: cautela com amostras pequenas.
- LPV/clique15/out **83,60%/85,44%**, pós **81,93%/84,49%**, 7d **83,72%/84,22%**. Recuperação diária não prova melhoria de carregamento; sem Web Vitals de campo.
- Semanas não sobrepostas2–8/out→9–15/out: exp.1014/2766=36,66%→1172/3100=37,81% (**+1,15p.p./+3,13%**); controle1072/2933=36,55%→2562/6724=38,10% (**+1,55p.p./+4,25%**). Diferença das evoluções relativas−1,12 pontos percentuais, das mudanças absolutas−0,41p.p. Diferença7d exp.−controle−0,30p.p., IC95%−2,36 a+1,77p.p. Janelas mistas, sem atribuição causal ao headline.
- Revisão versus snapshot15/out: somente controle14/out investimentoR$191,78→191,79 e impressões49723→49726; LPV964/Leads380 inalterados. Preservados os registros anteriores; baseline sem revisão.

### Decisão, gate e próximo passo

**Manter CRO-001 Em avaliação; nenhuma alteração da landing.** Próxima leitura:16/out completo; checkpoint exploratório14–16/out em17/out, sem critério de parada por primeiro intervalo favorável. Gate faltante é volume/cobertura/consistência com incerteza e mix, não publicação ou nova janela após convite. Plano mantido: MDE+3p.p., alfa bilateral5%, poder80%, referência aproximada4128LPV por período, não garantia nem critério único. Restam **3280LPV**; taxas recentes442,86LPV/dia(7d) e419,00(14d) projetam mais8dias completos, consulta de volume estimada **24/out**, condicionada ao tráfego. A projeção anterior24–25/out foi atualizada pelo volume observado, não por resultado favorável. Avaliar explicitamente antes de outro tratamento; sem suporte suficiente, inconclusivo.

Backlog preservado: contraste do CTA em teste separado após avaliar CRO-001; nenhum material extra necessário. Depoimentos/prints/ofertas/provas sociais somente reais, verificáveis, autorizados/anonimizados. Sem nova implementação, não foi repetida QA visual mobile; HTML normalizado reconfirmado equivalente ao tratamento já validado390×844/360×800. Não é novo teste Safari nem performance de campo.

**Escopo:** exclusivamente CRO_EXPERIMENTS.md no mesmo PR#16; nenhum merge dePR, auto-merge, deploy, alteraçãoMeta/Pixel/eventos/destinos/controle/experimental ou mensagem externa pelo agente. Artefatos atuais: `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-16/` (report.md, analysis.json, série diáriaGraph29/set–15/out, respostasMCP, auditsbaseline/7d/pós, validaçãoPages/live, history-validation.json, additional-validation.json, remote-verification.json). Helpers reutilizados apenas como código; nenhum snapshot anterior substituiu dados atuais.

## Acompanhamento diário — 2026-10-17

**Checkpoint exploratório de três dias completos cumprido; manter CRO-001 Em avaliação, resultado inconclusivo.** Execução às 09h America/Sao_Paulo; dados consolidados 12:02:51Z. Histórico integral da main e do PR #16, PRs abertos/fechados e commits consultados antes do diagnóstico. Worktree nova a partir da main `c961011`, incorporando histórico pendente; demais worktrees preservadas. Reutilizar o único PR aberto #16, documental, sem outro tratamento.

MCP oficial ad hoc inicializado, protocolo negociado `2025-11-25`, schemas/conta consultável/campos verificados; só leitura. Janelas e baseline conciliados exatamente em gasto/impressões/cliques/LPV/Leads com Graph GET diário29/set–16/out; aliases selecionados, atribuição unificada preservada, sem páginas/continuações pendentes. Excluir17/out incompleto. **Lead é proxy de clique antes da navegação, não entrada confirmada.** Baseline histórico36% sem denominador: descritivo, sem teste estatístico contra ele.

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-16 a 2026-10-16 | Experimental | R$ 101,13 | 21710 | 492 | 410 | 170 | 41,46% | R$ 0,59 |
| 1 | 2026-10-16 a 2026-10-16 | Controle | R$ 202,91 | 48403 | 1183 | 1030 | 391 | 37,96% | R$ 0,52 |
| 3 | 2026-10-14 a 2026-10-16 | Experimental | R$ 289,57 | 65510 | 1527 | 1258 | 519 | 41,26% | R$ 0,56 |
| 3 | 2026-10-14 a 2026-10-16 | Controle | R$ 576,85 | 143473 | 3414 | 2915 | 1146 | 39,31% | R$ 0,50 |
| 7 | 2026-10-10 a 2026-10-16 | Experimental | R$ 704,36 | 158410 | 3727 | 3127 | 1212 | 38,76% | R$ 0,58 |
| 7 | 2026-10-10 a 2026-10-16 | Controle | R$ 1411,56 | 368192 | 8330 | 7053 | 2664 | 37,77% | R$ 0,53 |
| 14 | 2026-10-03 a 2026-10-16 | Experimental | R$ 1264,14 | 298277 | 6994 | 5869 | 2184 | 37,21% | R$ 0,58 |
| 14 | 2026-10-03 a 2026-10-16 | Controle | R$ 2048,05 | 535708 | 12166 | 10331 | 3890 | 37,65% | R$ 0,53 |

**Avaliação:** 3d agora é integralmente pós-CRO-001; 7/14d misturam tratamentos. Baseline congelado29/set–12/out reconsultado sem revisão:1992/5387=36,98% e2901/7672=37,81%;13/out misto excluído. Pós14–16/out:519/1258=41,26% (Wilson95%38,57–44,00),1146/2915=39,31% (37,56–41,10). Experimental+4,28p.p./+11,57%, IC95% nominal+1,27 a+7,29; controle+1,50p.p./+3,97%, IC95%−0,58 a+3,58. Diferença entre mudanças+2,78p.p., IC95%−0,88 a+6,44; entre evoluções relativas+7,60 pontos percentuais. Diferença entre campanhas no pós+1,94p.p., IC95%−1,31 a+5,19. Aproximações binomiais/independência para eventos atribuídos; não ajustadas para leituras sequenciais, não causalidade randomizada nem autorização para parada por intervalo favorável. Somente1258LPV=30,47% da referência4128; quarta–sexta, sem fim de semana.

**Mix e revisões:** configuração dos anúncios ativos/conjuntos, bodies/titles, destinos/UTMs, tracking e atribuição iguais à consulta anterior; dois ativos experimentais, um controle, antigo pausado. ShareLPV de produtos atualizados81,77%pré→91,49%pós; CVR37,41%→41,70%(480/1151); texto4em135,03%→36,45%(39/107). Não atribuir toda a melhora ao headline. Android exp.39,77%→43,15%(337/781), iPhone32,11%→38,24%(182/476); controle40,47%→42,10%(698/1658) e33,91%→35,44%(443/1250), sem diagnóstico Safari. Stories exp.share88,58%→88,08%, CVR35,85%→41,25%; controle88,56%→87,14%,36,87%→37,99%. LPV/clique pós82,38%/85,38%; último dia83,33%/87,07%, sem Web Vitals de campo. Semanas não sobrepostas3–9→10–16/out: exp.35,45%→38,76%(+3,31p.p./+9,34%), controle37,40%→37,77%(+0,37p.p./+0,99%); diferença relativa+8,35 pontos percentuais, absoluta+2,94p.p., descritivo/misto. Revisão controle15/out:R$182,13→182,15, impressões45340→45344, LPV/Leads inalterados; snapshots preservados. Contagens breakdownsbaseline/7d/pós exatas; dispositivoexp.7d somaR$704,360001, resíduo−R$0,000001 (<1centavo), totais principais exatos.

**Publicação:** inicial1a377ea, built13/out23:42:37Z (20:42:37SãoPaulo) reconfirmada. Humano mesclou #19 no controle16/out14:51:22Z e #20 na experimental21:33:39Z; somente href/constante. Pages atual `c96101199f72fdf0c5a10d83850892bd9220060a`, built16/out21:34:15Z (18:34:15SãoPaulo); ambas públicas HTTP200 byte a byte iguais ao commit às12:03:34Zde17/out. Normalizando somente convites, ambos HTMLs inteiros idênticos ao tratamento inicial; conteúdo/CTA/Pixel/Lead preservados. Controle foi rotacionado pelo humano, nunca pelo agente. **Rotação não reinicia avaliação.** Timestamp do build não é exposição exata por visitante. NodeVM sem rede:11 verificações do CTA real aprovadas, Lead antes da navegação normal, delay150ms, sem eventoMeta real/join. Sem implementação nova: QA visual mobile não repetida, equivalência à versão validada390×844/360×800 confirmada, não Safari real.

**Decisão/gate:** manter tratamento; faltam volume, cobertura semanal/consistência e avaliação de incerteza/mix, não publicação ou convite. Plano original MDE+3p.p./alfa5% bilateral/poder80%/4128LPV aproximados preservado, não garantia nem critério único. Restam2870LPV; ritmos446,71(7d)/419,21(14d) por dia projetam mais7dias completos, consulta estimada24/out se tráfego persistir, não prazo de vitória. Próxima observação17/out completo, iniciando cobertura de fim de semana. Backlog contrasteCTA separado após avaliar explicitamente CRO-001; nenhum material extra agora. Provas sociais só reais/verificáveis/autorizadas/anonimizadas.

**Escopo:** somente CRO_EXPERIMENTS.md no mesmo [PR #16](https://github.com/ibombonato/promos-da-lidi/pull/16). Sem alteração das landings/Meta/Pixel/eventos/UTMs/destinos pelo agente, merge dePR/auto-merge/deploy, mensagem externa ou agendamento. Artefatos atuais sem secrets em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-17/`: report.md, analysis.json, daily-graph.json, respostasMCP, auditsbaseline/7d/pós, live-validation.json, history-validation.json, additional-validation.json, cta-validation.json e remote-verification.json. Helpers anteriores são só código; dados atuais reconsultados.

## Acompanhamento diário — 2026-10-18

**Decisão: manter CRO-001 Em avaliação, sem alterar landing; resultado ainda inconclusivo.** Execução às09h America/Sao_Paulo, métricas consolidadas12:02:49Z. Histórico integral da main atual e do único PR aberto#16, PRs fechados e commits consultados antes do diagnóstico. Worktree nova da main `c961011` incorporou histórico pendente; outras worktrees preservadas. Atualizar o mesmo [PR documental#16](https://github.com/ibombonato/promos-da-lidi/pull/16), sem outro experimento.

**Fator externo novo e relevante:** Graph GET de atividades da conta confirmou `update_campaign_budget` da experimental em **2026-10-17T23:40:22-03:00**, de **R$100 para R$150/dia (+50%)**; status transitório Processo pendente→Ativa às23:40:41. Readback atual: experimentalACTIVE/R$150, controleACTIVE/R$200. O MCP de atividades retornou vazio nas duas campanhas; o vazio não foi interpretado como ausência de edição. Anúncios ativos, conjuntos, copy/destinos/UTMs, tracking, atribuição e tratamento visível permanecem iguais à execução anterior. Mudança de orçamento não foi feita por este agente; não inferir identidade/autorização do autor. Não comprova alteração de qualidade nem causa de CVR, mas pode mudar entrega/leilão/mix posterior. Diferentemente de convite operacional, é um fator de confundimento real: **manter baseline/acumulado de headline, sinalizar17/out como dia de orçamento misto e apresentar sensibilidade14–16/out e dias completos desde18/out separadamente**; não reiniciar silenciosamente ou misturar efeito de escala com headline.

MCP oficial ad hoc inicializado, protocolo negociado2025-11-25 reutilizado; schemas/conta consultável/campos verificados, somente ferramentas de leitura. Quatro janelas/baseline conciliados exatamente em gasto/impressões/cliques/LPV/Leads com Graph GET diário29/set–17/out. Aliases selecionados, atribuição unificada preservada, sem páginas/continuações pendentes nas métricas. AtividadesGraph29 registros examinados com paginação esgotada. Excluir18/out parcial. **Lead é proxy de clique no CTA antes da navegação, não entrada confirmada no grupo.** Baseline histórico36% sem denominador é somente referência descritiva.

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-17 a 2026-10-17 | Experimental | R$ 95,13 | 19143 | 522 | 435 | 178 | 40,92% | R$ 0,53 |
| 1 | 2026-10-17 a 2026-10-17 | Controle | R$ 188,58 | 44988 | 1132 | 971 | 381 | 39,24% | R$ 0,49 |
| 3 | 2026-10-15 a 2026-10-17 | Experimental | R$ 288,33 | 62077 | 1514 | 1263 | 521 | 41,25% | R$ 0,55 |
| 3 | 2026-10-15 a 2026-10-17 | Controle | R$ 573,65 | 138737 | 3393 | 2922 | 1147 | 39,25% | R$ 0,50 |
| 7 | 2026-10-11 a 2026-10-17 | Experimental | R$ 699,62 | 157346 | 3739 | 3115 | 1242 | 39,87% | R$ 0,56 |
| 7 | 2026-10-11 a 2026-10-17 | Controle | R$ 1399,74 | 363245 | 8381 | 7103 | 2713 | 38,20% | R$ 0,52 |
| 14 | 2026-10-04 a 2026-10-17 | Experimental | R$ 1285,78 | 301821 | 7152 | 5995 | 2228 | 37,16% | R$ 0,58 |
| 14 | 2026-10-04 a 2026-10-17 | Controle | R$ 2158,58 | 564097 | 12866 | 10910 | 4138 | 37,93% | R$ 0,52 |

**CRO-001:** baseline29/set–12/out reconsultado sem revisão dos totais:1992/5387=36,98%,2901/7672=37,81%;13/out parcialmente exposto excluído. Pós14–17/out: experimental697/1693=41,17%,Wilson95%38,85–43,53,CPLR$0,55; controle1527/3886=39,29%,Wilson37,77–40,84,CPLR$0,50. Experimental+4,19p.p./+11,34% relativo,IC95%nominal+1,52 a+6,87; controle+1,48p.p./+3,92%,IC95%−0,40 a+3,36. Diferença entre mudanças+2,71p.p.,IC95%−0,56 a+5,98; entre evoluções relativas+7,42 pontos percentuais. Diferença entre campanhas posterior+1,87p.p.,IC95%−0,93 a+4,68. Aproximações binomiais/independência para eventos atribuídos, sem ajuste por consultas sequenciais, sem randomização/coorte deduplicada: não concluir causalidade/vitória. Somente1693LPV=41,01% da referência4128, quarta–sábado, sem domingo–terça. Janelas1/3d e acumulado14–17 são posteriores ao headline, mas incluem a edição tardia de orçamento em17/out;7/14d ainda misturam headlines.

**Sensibilidade anterior ao novo orçamento, reconsultada hoje:**14–16/out,519/1258=41,26% vs1146/2915=39,31%; diferença entre mudanças+2,78p.p.,IC95%−0,88 a+6,44, permanece inconclusiva. Essa segmentação documenta um evento externo observado, não substitui retrospectivamente o desfecho principal pelo mais favorável. A partir da próxima leitura, mostrar18/out em diante como fase distinta, mantendo a série completa.

**Mix e revisões:** anúncios/conjuntos estáveis, dois ativos experimentais/umcontrole e antigo pausado. Diferença bruta no antigo pausado foi apenasminiatura assinada; não é edição de criativo. Produtos atualizados shareLPV81,77%pré→90,55%pós,634/1533=41,36%; texto4em1 63/160=39,38%, volume pequeno. Androidsmartphone pós458/1062=43,13% vs945/2246=42,07%; iPhone239/630=37,94% vs577/1630=35,40%. Stories pósshare87,06%/86,39%,CVR41,04%/37,80%; feed69/153=45,10% vs170/334=50,90%; Reels22/62=35,48% vs87/193=45,08%. Não inferir defeitoSafari ou efeito causal a partir dessas diferenças. LPV/clique pós82,63%/85,48%; último dia83,33%/85,78%; sem WebVitals de campo. Semanas4–10→11–17/out: experimental34,24%→39,87%(+5,64p.p./+16,46%); controle37,43%→38,20%(+0,76p.p./+2,04%); diferença relativa+14,42 pontos percentuais e absoluta+4,87p.p., descritivo/misto. Revisões16/out: experimentalimpressões21710→21711; controle202,91→202,92 e48403→48405; LPV/Leads iguais. Preservados snapshots anteriores. Contagensbreakdownsbaseline/7d/pós exatas; resíduos monetários de ±R$0,000001 inferiores a um centavo, totaisMCP/Graph principais exatos.

**Publicação/integridade:** sem novo commit/PR de landing desde a consulta anterior. Pagesatual `c96101199f72fdf0c5a10d83850892bd9220060a`,built16/out21:34:15Z; inicialCRO-001 `1a377ea858b18189d7b40b1fd63990376e777712`,built13/out23:42:37Z/20:42:37SãoPaulo, reconfirmados na API. HTMLpúblicoHTTP200 de ambas byte a byte igual ao commit às12:02:32Zde18/out; normalizando somente convites, iguais ao tratamento inicial. Headline, CTA, CSS, Pixel/evento e handler preservados, href/constante coerentes. Rotações continuam operacionais, não reiniciam avaliação. NodeVMsemrede:11verificaçõesCTA aprovadas, sem emissãoMeta/joinWhatsApp. Sem implementação nova: não repetir QA visual mobile; equivalência ao tratamento previamente validado390×844/360×800 conferida, não testeSafari ou performance real.

**Gate/próximo passo:** volume/cobertura/consistência e avaliação do mix/atribuição, agora com fase de orçamento identificada. MDE+3p.p./alfa5%bilateral/poder80%/4128LPV aproximados mantidos, não garantia nem único critério. Restam2435LPV; ritmo histórico445,00(7d)/428,21(14d) projeta mais6dias e consulta24/out **apenas se ritmo persistir**; aumento de orçamento pode invalidar essa projeção. Não recalcular prazo assumindo crescimento proporcional ao orçamento. Próxima leitura inclui18/out completo, primeiro dia integral do orçamento novo; observar volume/CVR/CPL/mix versusfase anterior e controle, sem atribuir oscilações à headline. Avaliar explicitamente o experimento antes de outro tratamento; fechar inconclusivo se evidência continuar insuficiente, sem inventar vencedor ou esperar indefinidamente por um p-valor. BacklogcontrasteCTA separado, sem material extra agora; provas sociais somente reais/verificáveis/autorizadas/anonimizadas.

**Escopo:** somenteCRO_EXPERIMENTS.md no mesmoPR#16; sem alteraçãoMeta/landings/Pixel/eventos/UTMs/destinos, merge remoto/auto-merge/deploy, mensagens externas ou agendamentos. Artefatos atuais sem secrets em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-18/`:report.md,analysis.json,daily-graph.json,respostasMCP,auditsbaseline/7d/pós,campaign-config.json,graph-activities.json,live-validation.json,history-validation.json,additional-validation.json,cta-validation.json e verificação remota. Helpers anteriores reutilizados somente como código; dados atuais coletados nesta execução.

## Acompanhamento diário — 2026-10-19

**Decisão: manter CRO-001 Em avaliação; resultado inconclusivo, sem alterar a landing.** Execução iniciada às09h America/Sao_Paulo. Histórico integral da main e do PR documental#16, PRs abertos/fechados e commits consultados antes do diagnóstico. Worktree própria a partir de origin/main `c961011`, incorporando o histórico pendente por fast-forward local; outras worktrees preservadas. Único PR aberto#16, somente documentação, reutilizado sem novo experimento.

**Fontes:** MCP oficial ad hoc inicializado, protocolo negociado `2025-11-25` reutilizado; schemas somente leitura, conta consultável e campos confirmados. Totais das quatro janelas e baseline conciliados exatamente com Graph GET diário29/set–18/out em investimento/impressões/cliques/LPV/Leads; aliases selecionados, não somados, atribuição unificada preservada, sem páginas/continuações pendentes. Contagens dos breakdowns baseline/7d/pós/fase de orçamento exatas; resíduos de alocação monetária até±R$0,000001, inferiores a um centavo, sem divergência nos totais principais. Excluir19/out parcial. **Lead é proxy de clique no CTA antes do redirecionamento, não entrada confirmada no grupo.** Baseline histórico36% sem denominador é apenas descritivo.

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-18 a 2026-10-18 | Experimental | R$171,21 | 39922 | 882 | 732 | 286 | 39,07% | R$0,60 |
| 1 | 2026-10-18 a 2026-10-18 | Controle | R$228,25 | 55292 | 1287 | 1096 | 437 | 39,87% | R$0,52 |
| 3 | 2026-10-16 a 2026-10-18 | Experimental | R$367,47 | 80776 | 1896 | 1577 | 634 | 40,20% | R$0,58 |
| 3 | 2026-10-16 a 2026-10-18 | Controle | R$619,75 | 148688 | 3603 | 3097 | 1209 | 39,04% | R$0,51 |
| 7 | 2026-10-12 a 2026-10-18 | Experimental | R$757,14 | 173554 | 4100 | 3417 | 1370 | 40,09% | R$0,55 |
| 7 | 2026-10-12 a 2026-10-18 | Controle | R$1394,48 | 361020 | 8379 | 7119 | 2757 | 38,73% | R$0,51 |
| 14 | 2026-10-05 a 2026-10-18 | Experimental | R$1371,76 | 322135 | 7548 | 6317 | 2363 | 37,41% | R$0,58 |
| 14 | 2026-10-05 a 2026-10-18 | Controle | R$2305,79 | 600576 | 13687 | 11600 | 4418 | 38,09% | R$0,52 |

**CRO-001 — snapshot posterior atual:**14–18/out, cinco dias completos;13/out misto excluído. Baseline congelado29/set–12/out reconsultado sem revisão: experimental1992/5387=36,98%, controle2901/7672=37,81%. Pós experimental983/2425=40,54%, Wilson95%38,60–42,50, investimentoR$555,91/CPLR$0,57; controle1964/4982=39,42%, Wilson38,07–40,79, R$993,69/CPLR$0,51. Experimental+3,56p.p./+9,62% relativo, IC95%nominal da diferença+1,22 a+5,90; controle+1,61p.p./+4,26%, IC95%−0,13 a+3,35. Diferença entre mudanças **+1,95p.p., IC95%−0,97 a+4,86**, inclui zero; entre evoluções relativas+5,37 pontos percentuais. Somente2425LPV=58,75% da referência4128, quarta–domingo, ainda sem segunda/terça. Comparação observacional entre campanhas e antes/depois, não causalidade randomizada; aproximações binomiais para eventos atribuídos/dependentes, sem ajuste por consultas sequenciais. Não parar por intervalo nominal favorável. Janelas7/14d misturam headlines;1/3d e acumulado também abrangem fases distintas de orçamento.

### Primeiro dia integral do orçamento novo — diagnóstico separado

A mudança externa de R$100→R$150/dia em17/out23:40:22SãoPaulo foi reconfirmada por Graph GET; orçamento atual experimentalR$150/controleR$200, ambosACTIVE e sem nova alteração desde a consulta anterior. AtividadesGraph:31registros examinados, paginação esgotada, somente a mesma mudança e status transitório relevantes; MCP de atividades novamente vazio, não prova de ausência de edição. Nenhuma mudançaMeta pelo agente. **Não reiniciar baseline nem substituir o acumulado do headline.**17/out é transição;14–16/out é fase inteiramente anterior e18/out inicia fase posterior completa.

| Fase | LPV exp./controle | Leads exp./controle | CVR exp./controle | CPL exp./controle | Diferença entre mudanças vs baseline, IC95% |
|---|---|---|---|---|---|
| 14–16/out, antes do orçamento | 1258/2915 | 519/1146 | 41,26%/39,31% | R$0,56/R$0,50 | +2,78p.p. [−0,88;+6,44] |
| 17/out, transição tardia | 435/971 | 178/381 | 40,92%/39,24% | R$0,53/R$0,49 | +2,52p.p. [−3,28;+8,31] |
| 18/out, orçamento novo | 732/1096 | 286/437 | 39,07%/39,87% | R$0,60/R$0,52 | +0,03p.p. [−4,84;+4,91] |

No18/out, contra a média diária14–16/out: LPV experimental+74,56%, investimento+77,38%, CVR−2,18p.p., CPL+7,29%; controleLPV+12,80%, gasto+18,70%, CVR+0,56p.p., CPL+3,76%. **Um domingo versus quarta–sexta não isola efeito do orçamento nem da headline**; volume maior e taxa menor são observações, não evidência suficiente de degradação/escala causal. Sem extrapolação proporcional ao orçamento. O sinal agregado favorável diminuiu, mas não justifica reversão ou interrupção precoce.

**Mix/configuração:** anúncios ativos, conjuntos, bodies/titles completos, destinos/UTMs, tracking e atribuição iguais à execução anterior. Dois ativos experimentais e um controle; antigo pausado apresenta somente rotação da URL assinada da miniatura, demais campos idênticos. Pixel1504398471438133 e atribuição clique7d/visualização1d/vídeo-engajado1d preservados. Produtos atualizados shareLPV81,77%pré→89,15%pós; no18/out85,93%(246/629=39,11%), texto4em140/103=38,83%. Android18/out203/510=39,80%,share69,67%, controle307/707=43,42%,share64,51%; iPhone83/222=37,39%,controle127/386=32,90%. Stories18/out245/638=38,40%,share87,16%,controle345/896=38,50%,share81,75%; feed/Reels experimentais57/36LPV, cautela. Não inferir defeitoSafari. LPV/clique18/out82,99%/85,16%; pós82,74%/85,40%; sem WebVitals de campo. Semanas não sobrepostas5–11→12–18/out: experimental34,24%→40,09%(+5,85p.p./+17,09%relativo),controle37,07%→38,73%(+1,66p.p./+4,48%); diferença relativa+12,61 pontos percentuais, absoluta+4,19p.p., descrição mista. Diferença7d entre campanhas+1,37p.p.,IC95%−0,63 a+3,36. Revisões versus18/out: controle17/out impressões44988→44991,cliques1132→1133; nenhuma revisão de LPV/Leads/investimento ou baseline; snapshots anteriores preservados.

**Publicação/integridade:** nenhuma nova mudança de landing/PR desde a execução anterior. Pages atual `c96101199f72fdf0c5a10d83850892bd9220060a`,built16/out21:34:15Z; publicação inicial `1a377ea858b18189d7b40b1fd63990376e777712`,built13/out23:42:37Z/20:42:37SãoPaulo. API Pages e HTMLs públicos HTTP200 reconfirmados às12:02:10Zde19/out: ambas páginas byte a byte iguais ao commit, normalizando somente convites idênticas ao tratamento inicial. CTA/Pixel/Lead/headline preservados; rotações operacionais não reiniciam avaliação. Script real em NodeVM sem rede:11verificações aprovadas, sem emitir eventoMeta nem joinWhatsApp. Sem nova implementação: QA visual mobile não repetida; equivalência à versão validada390×844/360×800 reconfirmada, não testeSafari real nem performance de campo.

**Gate e próxima observação:** faltam volume/cobertura semanal/consistência e avaliação da fase de orçamento/mix/atribuição. Manter planoMDE+3p.p./alfa5%bilateral/poder80%/4128LPV aproximados, não garantia nem critério único. Restam1703LPV; ritmos históricos488,14(7d)/451,21(14d)LPV/dia projetam mais4dias completos, consulta de volume estimada23/out **somente se o ritmo persistir**, substituindo a projeção anterior24/out por volume observado, não por p-valor. Nova fase tem apenas um domingo: não tratar projeção como prazo garantido nem supor tráfego proporcional ao orçamento. Próxima leitura inclui19/out completo, primeira segunda-feira posterior, e segundo dia integral de orçamento novo. Avaliar explicitamente CRO-001 no checkpoint de volume com cobertura semanal e fases; se continuar sem suporte, registrar inconclusivo, não esperar indefinidamente por significância. Backlog: contrasteCTA como hipótese separada, não implementada agora; nenhum material extra necessário. Provas sociais somente reais/verificáveis/autorizadas/anonimizadas.

**Escopo:** exclusivamenteCRO_EXPERIMENTS.md no mesmo[PR#16](https://github.com/ibombonato/promos-da-lidi/pull/16); nenhuma alteraçãoMeta/landings/Pixel/eventos/UTMs/destinos, merge dePR/auto-merge/deploy, mensagens externas ou agendamento. Artefatos atuais em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-19/`:report.md,analysis.json,daily-graph.json,respostasMCP,auditsbaseline/7d/pós/orçamento,campaign-config.json,graph-activities.json,live-validation.json,history-validation.json,additional-validation.json,cta-validation.json e remote-verification.json. Helpers reutilizados somente como código; dados atuais reconsultados, sem substituir por snapshots anteriores.

## Acompanhamento diário — 2026-10-20

**Decisão:** manter CRO-001 **Em avaliação**, resultado inconclusivo; nenhuma alteração nas landings. Execução às09h America/Sao_Paulo; métricas consolidadas às12:04:03Z. Histórico integral da main e do único PR aberto#16, PRs fechados e commits consultados antes do diagnóstico. Worktree própria a partir de `origin/main` `1d09079`, incorporando o histórico pendente com ancestralidade preservada; demais worktrees intactas. Reutilizar o mesmo [PR documental#16](https://github.com/ibombonato/promos-da-lidi/pull/16), sem novo experimento.

**Fontes:** MCP oficial ad hoc inicializado, protocolo negociado2025-11-25 reutilizado; schemas somente leitura, conta consultável e campos confirmados. Erro500 transitório na consulta de baseline recuperado por retry. Totais1/3/7/14d e baseline conciliados exatamente com Graph GET diário29/set–19/out em gasto/impressões/cliques/LPV/Leads; aliases selecionados, atribuição unificada preservada, sem continuação/paginação pendente. Breakdowns baseline/7d/pós/orçamento: contagens exatas, resíduos monetários até±R$0,000001 (<1centavo), totais principais exatos. Excluir20/out parcial. **Lead é proxy de clique antes da navegação, não entrada confirmada.** Baseline histórico36% sem denominador, somente descritivo.

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-19 a 2026-10-19 | Experimental | R$148,72 | 38026 | 884 | 717 | 265 | 36,96% | R$0,56 |
| 1 | 2026-10-19 a 2026-10-19 | Controle | R$186,81 | 50230 | 1101 | 933 | 356 | 38,16% | R$0,52 |
| 3 | 2026-10-17 a 2026-10-19 | Experimental | R$415,06 | 97091 | 2288 | 1884 | 729 | 38,69% | R$0,57 |
| 3 | 2026-10-17 a 2026-10-19 | Controle | R$603,64 | 150514 | 3521 | 3000 | 1174 | 39,13% | R$0,51 |
| 7 | 2026-10-13 a 2026-10-19 | Experimental | R$796,66 | 185261 | 4359 | 3601 | 1424 | 39,54% | R$0,56 |
| 7 | 2026-10-13 a 2026-10-19 | Controle | R$1363,69 | 347308 | 8120 | 6905 | 2685 | 38,88% | R$0,51 |
| 14 | 2026-10-06 a 2026-10-19 | Experimental | R$1444,72 | 338132 | 7879 | 6570 | 2479 | 37,73% | R$0,58 |
| 14 | 2026-10-06 a 2026-10-19 | Controle | R$2412,81 | 627168 | 14266 | 12082 | 4612 | 38,17% | R$0,52 |

**CRO-001 — snapshot posterior14–19/out:** seis dias completos;13/out misto excluído. Baseline29/set–12/out reconsultado sem revisão:1992/5387=36,98%,2901/7672=37,81%. Pós experimental1248/3142=39,72%, Wilson95%38,02–41,44, investimentoR$704,63/CPLR$0,56; controle2320/5915=39,22%, Wilson37,99–40,47, R$1180,50/CPLR$0,51. Experimental+2,74p.p./+7,42%relativo, IC95%nominal+0,60 a+4,88; controle+1,41p.p./+3,73%, IC95%−0,24 a+3,06. Diferença entre mudanças **+1,33p.p., IC95%−1,37 a+4,04**, inclui zero; diferença entre evoluções relativas+3,69pontos percentuais. Volume76,11% da referência4128LPV; quarta–segunda, ainda semterça. O sinal favorável diminuiu novamente. Aproximações binomiais/independência para eventos atribuídos/dependentes, sem ajuste sequencial, randomização ou coorte deduplicada; não parar por intervalo nominal favorável. Janelas7/14d misturam headlines; acumulado também inclui fases de orçamento.

**Orçamento/fases:** Graph GET32atividades com paginação esgotada, sem nova edição relevante; experimental ACTIVE/R$150dia, controle ACTIVE/R$200dia. Mesma edição externa100→150 em17/out23:40:22SãoPaulo/status transitório reconfirmados; MCP de atividades vazio não prova ausência deedição. Preservar baseline/acumulado;17/out transição.14–16/out:519/1258=41,26% versus1146/2915=39,31%, CPLR$0,56/R$0,50, diferença entre mudanças+2,78p.p.IC95%−0,88 a+6,44.18–19/out:551/1449=38,03% versus793/2029=39,08%, CPLR$0,58/R$0,52, diferença entre mudanças versus baseline−0,22p.p.IC95%−3,91 a+3,46. Contra14–16/out, médiaLPV/dia experimental+72,77%, gasto/dia+65,73%, CVR−3,23p.p., CPL+4,07%; controleLPV/dia+4,41%, gasto/dia+7,93%, CVR−0,23p.p., CPL+3,98%. Comparação domingo/segunda versusquarta–sexta não isola orçamento/headline/tráfego nem autoriza reversão. Usar médias diárias dos dois períodos, não total de dois dias contra um dia.

**Mix/configuração:** anúncios ativos/conjuntos, bodies/titles completos, destinos/UTMs, tracking e atribuição idênticos àconsulta19/out; diferença bruta somente miniatura assinada no antigo pausado. Dois anúncios ativos experimentais/umcontrole, Pixel1504398471438133, clique7d/visualização1d/vídeoengajado1d preservados. Principal anúncio shareLPV81,77%pré→89,02%pós (1114/2797=39,83%); texto4em1:134/345=38,84%. Android pós857/2076=41,28%, controle1494/3529=42,33%; iPhone391/1065=36,71%,817/2371=34,46%; não inferir falhaSafari. LPV/clique19/out81,11%/84,74%, pós82,36%/85,29%; sem WebVitals de campo. Semanas não sobrepostas6–12→13–19/out: experimental35,53%→39,54% (+4,01p.p./+11,29%relativo), controle37,22%→38,88% (+1,66p.p./+4,47%); diferença relativa+6,82pontos percentuais e absoluta+2,35p.p., diagnóstico misto não causal. Diferença7d entre campanhas+0,66p.p., IC95%−1,31 a+2,63. Revisão única versus19/out: controle18/out impressões55292→55293; LPV/Leads/gasto/baseline inalterados, snapshots preservados.

**Publicação/integridade:** humano mesclou [PR#21](https://github.com/ibombonato/promos-da-lidi/pull/21) em20/out04:30:28Z (01:30:28SãoPaulo): somente href/WHATSAPP_GROUP_URL em `index4_li.html`; experimental semmudança. Pages atual `1d09079ba18a58825426bb28476784b4818ae6c7`, built20/out04:31:05Z (01:31:05SãoPaulo); inicialCRO-001 `1a377ea858b18189d7b40b1fd63990376e777712`, built13/out23:42:37Z (20:42:37SãoPaulo), reconfirmadoAPI. Ambas públicasHTTP200, byte a byte iguais ao commit; normalizando somente convites, HTMLs inteiros iguais ao tratamento inicial. Controle rotacionado pelo humano, nunca pelo agente; manutenção não reiniciaCRO-001. CTA/Pixel/evento/headline preservados; NodeVM semrede:11verificações aprovadas, sem eventoMeta/joinWhatsApp. Sem implementação nova: QA visual mobile não repetida; equivalência ao tratamento jávalidado390×844/360×800 confirmada, nãoSafari real.

**Gate/próximo passo:** volume/cobertura semanal/consistência, mix/atribuição e fases de orçamento. Plano MDE+3p.p./alfa5%bilateral/poder80%/4128LPVaproximados mantido, não garantia nem critério único; restam986LPV. Ritmos514,43(7d)/469,29(14d)LPV/dia projetam mais2–3dias completos, consulta22–23/out se persistirem, não prazo garantido ou extrapolação proporcional ao orçamento. Próxima leitura20/out completo, completando primeira cobertura de todos os dias da semana; no checkpoint avaliar explicitamenteCRO-001/fases/incerteza, fechar inconclusivo se insuficiente, sem esperar indefinidamente por p-valor. Backlog: contrasteCTA separado após avaliarCRO-001, sem material extra agora; provas sociais sóreais/verificáveis/autorizadas/anonimizadas.

**Escopo:** exclusivamente `CRO_EXPERIMENTS.md` no mesmoPR#16; sem alteraçãoMeta/landings/Pixel/eventos/UTMs/destinos, merge remoto/auto-merge/deploy, mensagem externa ou agendamento. Artefatos atuais em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-20/`:report.md,analysis.json,daily-graph.json,respostasMCP,audits,campaign-config.json,graph-activities.json,live-validation.json,history-validation.json,additional-validation.json,cta-validation.json,remote-verification.json. Helpers reutilizados como código, dados coletados nestaexecução.

## Acompanhamento diário — 2026-10-21

**Decisão:** manter CRO-001 **Em avaliação**, resultado inconclusivo; nenhuma alteração nas landings. Execução iniciada às 09h America/Sao_Paulo. Histórico integral da main e do único PR aberto #16, PRs fechados e commits consultados antes do diagnóstico. Worktree isolada da main `1d09079` incorporou o histórico pendente por fast-forward; outras worktrees intactas. Reutilizar o [PR documental #16](https://github.com/ibombonato/promos-da-lidi/pull/16), sem outro experimento.

**Fontes:** MCP oficial ad hoc inicializado, protocolo negociado `2025-11-25` reutilizado; schemas somente leitura, conta consultável e campos confirmados. Totais 1/3/7/14d e baseline conciliados exatamente em gasto/impressões/cliques/LPV/Leads com Graph GET diário 29/set–20/out; aliases selecionados, atribuição unificada preservada, sem continuação/paginação pendente. Anomalia Graph: consultas diárias com ações retornaram gasto/impressões zerados, mesmo em retry sem `cost_per_action_type`; GET separado de entrega recuperou valores reais. Série final é junção verificável por campanha/data de duas respostas atuais, não imputação; raws e proveniência preservados em `daily-graph-actions-raw.json`, `graph-delivery-daily-*.json`, `daily-graph-provenance.json`. Conciliação exata com MCP, sem aceitar zeros como ausência de entrega nem usar snapshots antigos. Breakdowns baseline/7d/pós/orçamento com contagens exatas e resíduos monetários inferiores a um centavo. Excluir 21/out parcial. **Lead é proxy de clique antes da navegação, não entrada confirmada. Baseline histórico 36%, sem denominador, é apenas descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-20 a 2026-10-20 | Experimental | R$150,28 | 35517 | 796 | 661 | 220 | 33,28% | R$0,68 |
| 1 | 2026-10-20 a 2026-10-20 | Controle | R$196,29 | 51090 | 1155 | 971 | 366 | 37,69% | R$0,54 |
| 3 | 2026-10-18 a 2026-10-20 | Experimental | R$470,23 | 113466 | 2562 | 2110 | 771 | 36,54% | R$0,61 |
| 3 | 2026-10-18 a 2026-10-20 | Controle | R$611,37 | 156615 | 3543 | 3000 | 1159 | 38,63% | R$0,53 |
| 7 | 2026-10-14 a 2026-10-20 | Experimental | R$854,93 | 198120 | 4611 | 3803 | 1468 | 38,60% | R$0,58 |
| 7 | 2026-10-14 a 2026-10-20 | Controle | R$1376,81 | 345081 | 8090 | 6886 | 2686 | 39,01% | R$0,51 |
| 14 | 2026-10-07 a 2026-10-20 | Experimental | R$1524,44 | 351870 | 8180 | 6805 | 2560 | 37,62% | R$0,60 |
| 14 | 2026-10-07 a 2026-10-20 | Controle | R$2537,78 | 655518 | 14964 | 12657 | 4837 | 38,22% | R$0,52 |

**CRO-001 — snapshot posterior 14–20/out:** sete dias completos, primeira cobertura quarta–terça; 13/out misto excluído. Baseline congelado 29/set–12/out reconsultado sem revisão: 1992/5387=36,98%, 2901/7672=37,81%. Pós experimental 1468/3803=38,60%, Wilson95%37,07–40,16, CPLR$0,58; controle 2686/6886=39,01%, Wilson37,86–40,16, CPLR$0,51. Experimental +1,62p.p./+4,39% relativo, IC95% nominal −0,39 a+3,64; controle +1,19p.p./+3,16%, IC95%−0,39 a+2,78. **Diferença entre mudanças +0,43p.p., IC95%−2,13 a+2,99**; entre evoluções relativas +1,23 pontos percentuais. Vantagem acumulada próxima de zero; nenhum vencedor/perdedor. Volume92,13% da referência4128LPV. Janela7d agora integralmente pós-headline;14d mistura versões; acumulado inclui fases de orçamento. Intervalos binomiais aproximados para eventos atribuídos/dependentes, sem ajuste sequencial, randomização ou coorte deduplicada; não parar por primeiro p-valor favorável.

**Orçamento/fases:** edição externa R$100→150/dia em17/out23:40:22SãoPaulo reconfirmada;17/out é transição. Atual experimentalACTIVE/R$150, controleACTIVE/R$200, sem nova edição relevante; Graph38atividades/paginação esgotada, MCPatividades vazio não prova ausência.14–16/out:519/1258=41,26% vs1146/2915=39,31%;18–20/out:771/2110=36,54% vs1159/3000=38,63%, CPLR$0,61/R$0,53. Nova fase versus baseline: diferença entre mudanças−1,26p.p.,IC95%−4,44 a+1,92. Médias diárias experimentais419,33→703,33LPV(+67,73%),gasto+62,39%,CVR−4,72p.p.,CPL+9,31%;controle971,67→1000LPV(+2,92%),gasto+5,98%,CVR−0,68p.p.,CPL+4,79%. Cada fase tem3dias inclusivos; domingo–terça versus quarta–sexta não isola orçamento/headline/qualidade do tráfego. Queda experimental39,07→36,96→33,28% merece acompanhamento, mas não prova causa nem justifica reversão automática. Preservar baseline/acumulado.

**Mix/configuração/revisões:** ativos/conjuntos/copy completa/destinos/UTMs/tracking/atribuição idênticos à consulta20/out; única diferença bruta é miniatura assinada no antigo pausado, restantes campos idênticos. Dois ativos experimentais/umcontrole,Pixel1504398471438133,clique7d/visualização1d/vídeoengajado1d. ShareLPVprincipal81,77%pré→88,25%pós(1300/3356=38,74%);texto4em1:168/447=37,58%. Androidpós1013/2527=40,09% vs1744/4169=41,83%;iPhone455/1275=35,69% vs933/2702=34,53%;sem inferir falhaSafari. Storiespós1279/3343=38,26% vs2207/5886=37,50%,shares87,90%/85,48%. LPV/clique20/out83,04%/84,07%,pós82,48%/85,12%,sem WebVitals de campo. Semanas7–13→14–20/out:experimental36,38→38,60%(+2,23p.p./+6,12%relativo),controle37,27→39,01%(+1,73p.p./+4,65%);diferença relativa+1,47pontos percentuais,absoluta+0,49p.p.,descrição não causal,janela anterior inclui dia misto. Revisões19/out:experimentalR$148,72→148,74/impressões38026→38027;controleR$186,81→186,83/impressões50230→50232;LPV/Leads/baseline inalterados,snapshots preservados.

**Publicação/QA:** sem novo PR/commit de landing. Pages `1d09079ba18a58825426bb28476784b4818ae6c7`,built20/out04:31:05Z; inicial `1a377ea858b18189d7b40b1fd63990376e777712`,built13/out23:42:37Z(20:42:37SãoPaulo),reconfirmadosAPI. Ambas públicasHTTP200/byte a byte iguais ao commit; normalizando apenas convites, iguais ao tratamento inicial. Headline/CTA/CSS/scripts/Pixel/Lead preservados; rotações operacionais não reiniciam avaliação. NodeVM sem rede:11verificações aprovadas,nenhum eventoMeta oujoinWhatsApp. Sem implementação nova,QAvisualmobile não repetida; equivalência à versão validada390×844/360×800 conferida,nãoSafari real ou performance de campo.

**Gate/próximo passo:** cobertura semanal completa; restam325LPV para checkpoint4128,não vitória automática. PlanoMDE+3p.p./alfa5%bilateral/poder80% preservado,não garantia. Ritmos543,29(7d)/486,07(14d)LPV/dia projetam mais1dia completo,consulta22/out se persistirem,não prazo garantido ou extrapolação proporcional ao orçamento. Próxima leitura21/out completo; se atingir referência de volume, avaliar explicitamenteCRO-001 com controle/fases/mix/consistência/incerteza; continuando sem suporte, registrar conclusão inconclusiva,sem esperar indefinidamente por significância. Não iniciar tratamento simultâneo. BacklogcontrasteCTA separado,sem material extra agora; provas sociais apenas reais/verificáveis/autorizadas/anonimizadas.

**Escopo:** somente `CRO_EXPERIMENTS.md` no mesmoPR#16;sem alteraçãoMeta/landings/Pixel/eventos/UTMs/destinos,merge remoto/auto-merge/deploy,mensagens externas ouagendamentos. Artefatos atuais: `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-21/` (`report.md`,`analysis.json`,série diária/raws/proveniênciaGraph,respostasMCP,audits,`campaign-config.json`,`graph-activities.json`,`live-validation.json`,`history-validation.json`,`additional-validation.json`,`cta-validation.json`,`remote-verification.json`). Helpers reutilizados somente como código;dados atuais coletados nesta execução.

## Acompanhamento diário — 2026-10-22

**Decisão: encerrar CRO-001 como Inconclusivo no checkpoint planejado e manter a landing publicada.** Execução iniciada às09h America/Sao_Paulo. Histórico integral da main atual e do único PR aberto#16, PRs fechados/commits consultados antes do diagnóstico. Worktree isolada criada de origin/main `e50f375`, incorporando a ancestralidade do histórico pendente sem tocar outras worktrees. Reutilizar o mesmo [PR documental#16](https://github.com/ibombonato/promos-da-lidi/pull/16); somente CRO_EXPERIMENTS.md. Nenhuma reversão ou implementação nova.

**Fontes:** MCP oficial ad hoc, protocolo negociado2025-11-25, schemas somente leitura, conta consultável e campos verificados. Quatro janelas, baseline, acumulado14–21/out e anúncios21/out conciliados exatamente com Graph GET em gasto/impressões/cliques/LPV/Leads; aliases selecionados, atribuição unificada preservada, sem continuação/paginação pendente. Breakdowns baseline/7d/pós/orçamento com contagens exatas, máximo resíduo monetárioR$0,000001. Hoje a consulta diária combinada retornou entrega normalmente; não reutilizar junção/snapshots de ontem. Excluir22/out incompleto. **Lead é proxy de clique no CTA antes da navegação, não entrada confirmada; baseline histórico36% sem denominador apenas descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques no link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-21 a 2026-10-21 | Experimental | R$141,66 | 26791 | 646 | 543 | 208 | 38,31% | R$0,68 |
| 1 | 2026-10-21 a 2026-10-21 | Controle | R$169,63 | 38952 | 866 | 741 | 280 | 37,79% | R$0,61 |
| 3 | 2026-10-19 a 2026-10-21 | Experimental | R$440,68 | 100337 | 2326 | 1921 | 693 | 36,07% | R$0,64 |
| 3 | 2026-10-19 a 2026-10-21 | Controle | R$552,77 | 140277 | 3122 | 2645 | 1002 | 37,88% | R$0,55 |
| 7 | 2026-10-15 a 2026-10-21 | Experimental | R$900,22 | 202336 | 4722 | 3916 | 1500 | 38,30% | R$0,60 |
| 7 | 2026-10-15 a 2026-10-21 | Controle | R$1354,67 | 334310 | 7803 | 6663 | 2586 | 38,81% | R$0,52 |
| 14 | 2026-10-08 a 2026-10-21 | Experimental | R$1600,83 | 362181 | 8455 | 7022 | 2649 | 37,72% | R$0,60 |
| 14 | 2026-10-08 a 2026-10-21 | Controle | R$2637,09 | 675012 | 15383 | 13031 | 4980 | 38,22% | R$0,53 |

**CRO-001 — conclusão no checkpoint:** baseline congelado29/set–12/out reconsultado sem revisão1992/5387=36,98%,2901/7672=37,81%;13/out misto excluído. Principal14–21/out:experimental1676/4346=38,56%,Wilson95%37,13–40,02,R$996,59/CPLR$0,59;controle2966/7627=38,89%,Wilson37,80–39,99,R$1546,46/CPLR$0,52. Experimental+1,59p.p./+4,29%relativo,IC95%nominal−0,35 a+3,52;controle+1,08p.p./+2,84%,IC95%−0,47 a+2,62. **Diferença entre mudanças+0,51p.p.,IC95%−1,97 a+2,99**; diferença das evoluções relativas+1,45pontos percentuais. CPL+1,93%/−3,55% sobre valores não arredondados. Volume4346LPV=105,28%da referência4128 e cobertura completa de dias da semana em oito dias. MDE+3p.p./alfa5%bilateral/poder80% eram planejamento, não garantia/critério único. ICs aproximados para eventos atribuídos/dependentes, sem ajuste sequencial/randomização/coorte deduplicada. Não comprovado ganho, prejuízo, equivalência ou ausência de efeito; sinais variam entre fases. **Encerrar Inconclusivo**, não continuar à espera de p-valor. Manter headline por continuidade, não como vencedora; sem evidência para reversão. Leituras seguintes não reabrem silenciosamente essa avaliação. Janela14d mistura headlines, não mede efeito puro.

**Mudança externa nova — não normalizar como miniatura/cursor:** experimental agora tem quatro anúncios ativos, dois novos `120252297350870505` e `120252297350880505`, criados21/out23:23:40/23:33:46SãoPaulo, primeira entrega23:31:51/23:43:24. MCP atividades e Graph GET confirmam. Os dois usamindex3/UTMs/Pixel1504398471438133 preservados; novos IDs de criativo, CTA de anúncioSEE_DETAILS (anterioresLEARN_MORE) e variantes de títulos/copy; um contém sete bodies, outro duas. Metadados inspecionados, não análise visual das mídias. Anúncios anteriores/conjuntos/atribuição e orçamentos permanecem semanticamente iguais; diferença adicional no antigo pausado é apenasminiatura assinada. Em21/out, novos juntosR$0,87/178impressões/5cliques/4LPV/3Leads;0,74%dosLPVdiários e0,09%do acumulado. Amostra não permite avaliar criativos ou atribuir a eles recuperação33,28→38,31%. Preservar principal14–21/out; sensibilidade excluindo apenasnovos anúncios1673/4342=38,53%,diferençaentremudanças+0,48p.p.,IC95%−2,00 a+2,95; sensibilidade14–20/out+0,43p.p.,IC95%−2,13 a+2,99. Ambas inconclusivas; não escolher janela favorável nem resetarCRO-001. Graph59atividades com paginação esgotada; filtro ampliado para IDs novos/conjuntos, sem depender apenas dos IDs conhecidos anteriormente.

**Orçamento/fases:** experimentalACTIVE/R$150dia,controleACTIVE/R$200dia,sem nova edição de orçamento; externa100→150em17/out23:40:22reconfirmada.14–16/out:519/1258=41,26%vs1146/2915=39,31%,CPLR$0,56/R$0,50.17/outtransição preservado.18–21/out:979/2653=36,90%vs1439/3741=38,47%,CPLR$0,63/R$0,54,diferençaentremudançasvsbaseline−0,73p.p.,IC95%−3,67 a+2,21. Comparar médias inclusivas3diasvs4dias:experimental419,33→663,25LPV/dia(+58,17%),gasto/dia+58,48%,CVR−4,35p.p.,CPL+12,02%;controle971,67→935,25LPV/dia(−3,75%),gasto/dia+1,54%,CVR−0,85p.p.,CPL+7,82%. Dias da semana diferentes e lançamento tardio de anúncios não isolam orçamento/headline/tráfego. Nenhuma alteraçãoMeta pelo agente.

**Mix/revisões:** shareLPVprincipal81,77%pré→87,57%pós(1470/3806=38,62%);texto4em1203/536=37,87%. Androidpós1172/2907=40,32%vs1930/4643=41,57%;iPhone504/1438=35,05%vs1027/2969=34,59%. Stories1448/3799=38,12%vs2437/6494=37,53%,shares87,41%/85,14%;não inferir falhaSafari. LPV/clique21/out84,06%/85,57%,pós82,67%/85,16%,semWebVitalsdecampo. Semanas8–14→15–21/out:experimental36,99→38,30%(+1,31p.p./+3,55%),controle37,59→38,81%(+1,22p.p./+3,24%),descrição observacional/janelaanterior mista. Revisões20/out:experimental35517→35519impressões;controleR$196,29→196,31,51090→51093impressões;LPV/Leads/baselineinalterados,snapshotspreservados.

**Publicação/QA:** main/Pages`e50f3753da1a9d5a416eed3d030780045f2dfdad`,built22/out01:21:56Z(21/out22:21:56SãoPaulo). Novo commitexterno muda apenasindex.html, nenhuma dasduaslandingsanalisadas. InicialCRO-001`1a377ea858b18189d7b40b1fd63990376e777712`,built13/out23:42:37Z(20:42:37SãoPaulo). Ambas públicasHTTP200/byte a byte iguais aocommit,normalizando apenasconvites iguais aotratamentoinicial. Headline/CTA/CSS/scripts/Pixel/Lead preservados;rotaçõesoperacionais não reiniciamavaliação. NodeVMsemrede11verificaçõesaprovadas,sem eventoMeta/joinWhatsApp. Sem nova implementação,não repetirQAvisualmobile;equivalência àversãovalidada390×844/360×800conferida,nãoSafariouperformance real.

**Próximo passo/gate concreto:** CRO-001 encerrado; não aguardar mais dados para tentar torná-lo vencedor. Monitorar22/outcompleto na próximaleitura,primeirodiaintegral dosquatroanúncios,com distribuição poranúncio/CVR/CPL e revisão daestabilidade da referência paraopróximoteste. Não implementarcontrasteCTAhojeemcima dolançamentoexterno;umaprincipalvariávelporvez. BacklogcontrasteCTA permanecepriorizado,sem materialextra,semIDdeexperimento atribuídosemimplementação. Nova preparação deve pré-registrar baseline compatível com anovacomposição e checkpoints próprios; não impor espera arbitrária ou reutilizar4128como limiaruniversal. Materiais reais/autorizados/verificáveis sóparaeventuais hipótesesdeprovasocial.

**Escopo:** apenasCRO_EXPERIMENTS.mdnomesmoPR#16;semalteraçãoMeta/landings/Pixel/eventos/UTMs/destinos,mergeremoto/auto-merge/deploy,mensagensexternasouagendamentos. Evidências atuais em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-22/`:report.md,analysis.json,daily-graph.json,respostasMCP,auditsbaseline/7d/pós/orçamento,campaign-config.json,graph-activities-expanded.json,ad-daily-21.json,live-validation.json,history-validation.json,additional-validation.json,cta-validation.json e remote-verification.json. Helpers reutilizados somente como código; nenhuma métrica substituída por snapshot antigo.

## Acompanhamento e retomada proativa — 2026-10-23

**Decisão: implementar CRO-002 em PR, não aguardar novamente CRO-001.** Histórico integral da main e do PR#16 lido; PRs abertos/fechados e publicação consultados. CRO-001 permanece **Inconclusivo**, encerrado em22/out; endpoint14–21/out reconsultado com os mesmos LPV/Leads/gasto:38,56% versus38,89%; diferença entre mudanças+0,51p.p.,IC95%−1,97a+2,99. Nenhum novo dia foi acrescentado oportunisticamente a esse desfecho.

**Diagnóstico de atuação:** houve acompanhamento diário documentado de14a22/out, mas preparação/solicitação de materiais não evoluiu de forma suficiente enquanto o tratamento era avaliado. Não confundir monitoramento com melhoria comprovada nem usá-lo para perpetuar espera após encerrar teste. A cobrança do responsável motivou auditoria operacional e uma entrega concreta nesta execução.

**Falha operacional atual:** disparo automático23/out12:00:14Z falhou antes da análise com `GatewayUnavailableError/profile_parked`, conflito de credencial Telegram entre default/analyst. Scheduler running/enabled não demonstra execução saudável. Análise abaixo executada efetivamente nesta sessão manual; não alegar execução automática hoje. Prompt do próprio job714c96de5c45 atualizado e relido exatamente: entrega concreta diária, backlog ativo, pedidos de material, gates específicos, encerramento de testes e alerta de bloqueios. Horário09hSãoPaulo e transporte local preservados. Recuperação do gateway/ponte Telegram encaminhada ao operador @hermes, **ainda não comprovada**; outros perfis/serviços/credenciais não foram alterados. Próxima execução agendada24/out12:00Z, não garantia de conclusão.

### Métricas atuais — snapshot23/out15:28Z, dias completos de São Paulo

MCP oficial read-only inicializado, protocolo negociado reutilizado, conta/campos/schemas confirmados; janelas conciliadas exatamente com Graph GET diário29/set–22/out em gasto,impressões,cliques,LPV,Leads. Aliases selecionados, não somados; paginação/continuações verificadas. Hoje23/out excluído. **Lead é proxy de clique antes de navegar, não entrada confirmada. Baseline histórico36% sem denominador é descritivo.**

| Dias | Período inclusivo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-22–2026-10-22 | Experimental | R$ 247,29 | 48563 | 1011 | 882 | 349 | 39,57% | R$ 0,71 |
| 1 | 2026-10-22–2026-10-22 | Controle | R$ 186,72 | 38587 | 958 | 826 | 311 | 37,65% | R$ 0,60 |
| 3 | 2026-10-20–2026-10-22 | Experimental | R$ 539,23 | 110873 | 2453 | 2086 | 777 | 37,25% | R$ 0,69 |
| 3 | 2026-10-20–2026-10-22 | Controle | R$ 552,66 | 128632 | 2979 | 2538 | 957 | 37,71% | R$ 0,58 |
| 7 | 2026-10-16–2026-10-22 | Experimental | R$ 1055,44 | 229676 | 5233 | 4380 | 1676 | 38,26% | R$ 0,63 |
| 7 | 2026-10-16–2026-10-22 | Controle | R$ 1359,24 | 327553 | 7683 | 6568 | 2522 | 38,40% | R$ 0,54 |
| 14 | 2026-10-09–2026-10-22 | Experimental | R$ 1754,72 | 388406 | 8936 | 7480 | 2848 | 38,07% | R$ 0,62 |
| 14 | 2026-10-09–2026-10-22 | Controle | R$ 2710,93 | 683894 | 15667 | 13292 | 5084 | 38,25% | R$ 0,53 |

**Evolução semanal9–15/out→16–22/out:** experimental37,81→38,26% (+0,46p.p./+1,21%relativo),controle38,10→38,40% (+0,30p.p./+0,78%); diferença entre evoluções relativas+0,44pontos percentuais, descritiva. Não atribuir ao CRO-002 não publicado.

**Mix e fatores externos:** quatro anúncios experimentais ativos, um antigo pausado; um controle ativo. Em22/out os dois novos anúncios anteriormente identificados somaram15LPV/9Leads/R$4,07; participação1,70% dos882LPV. Principal anúncio756LPV/297Leads; texto 4 em 1: 111 LPV/43 Leads. Contagens/gasto por anúncio e breakdowns conciliados ao total. Isso não caracteriza teste50/50 de criativos. Android experimental230/561=41,00%,iPhone119/320=37,19%, sem evidência de defeitoSafari. Orçamento experimental segueR$150/dia; gasto22/outR$247,29 não foi tratado como prova de edição do orçamento. Controle teve mudança externaR$200→170/dia em22/out09:05:28SãoPaulo, reconfirmada por atividades/readback;22/out é transição do controle. Comparações entre campanhas não isolam a landing. Três outros IDs em atividades de primeira entrega não retornaram objetos consultáveis (Graph100/subcode33); não inventar status ou criativo, guardar limitação. Ad insights conciliados representam os IDs com entrega reportada na janela.

**Publicação atual:** main48a3628 (PR#22 humano, somente convite experimental), Pagesbuilt23/out14:47:30Z; HTMLpúblicoHTTP200 de ambas as páginas conferiu byte a byte com main. Convite atual preservado nohref e constante; manutenção operacional não reiniciaCRO-001. Nenhum merge/deploy pelo agente.

## CRO-002 — Aumentar a legibilidade do botão de entrada

**Data de criação:** 2026-10-23
**Status:** Em PR
**Data de publicação:** Pendente — não publicado por esta execução.
**Commit de publicação:** Pendente.
**Pull Request:** [#16 — CRO-002](https://github.com/ibombonato/promos-da-lidi/pull/16), convertido do acompanhamento documental para evitar PR paralelo/duplicado; todo histórico preservado.
**Branch de trabalho isolada:** `cro/CRO-002-cta-contrast-2026-10-23`, com ancestralidade do histórico pendente e main atual; envio fast-forward à branch já vinculada ao PR#16.
**Screenshot mobile:** [390×844](cro/screenshots/CRO-002-mobile.png), [360×800](cro/screenshots/CRO-002-mobile-360x800.png) e [antes390×844](cro/screenshots/CRO-002-before-390x844.png).

### Problema, evidência e hipótese pré-registrada

O texto branco do botão atual sobre verde tem contraste **2,38:1–3,15:1**, abaixo da referênciaWCAG1.4.3de4,5:1 para texto normal; fonte real16,38pxem390e15,12pxem360. **Escurecer somente o fundo do mesmo CTA para facilitar sua leitura pode aumentar a propensão ao clique por LPV.** Evidência objetiva de acessibilidade não demonstra abandono causado pela cor nem prevê ganho de conversão. Não alterar copy, posição, dimensões ou headline ao mesmo tempo. ICE qualitativo: impacto6,confiança9 na falha técnica(não no ganho),facilidade9.

### Alteração realizada

Exclusivamente duas variáveisCSS usadas no gradiente `.cta` em `index3.html`:

| Variável | Antes | Depois | Contraste com branco depois |
|---|---|---|---|
| `--green-2` | `#0bc247` | `#087f2c` | 5,14:1 |
| `--green` | `#09a83a` | `#086b29` | 6,68:1 |

Cor verde e texto branco mantidos. Todo o restante do HTML é idêntico àmain: copy, prova social existente(não validada), geometria, foco, hover, recursos, links/convite/UTMs, Pixel e scripts/eventos/delay150ms. Controle idêntico byte a byte. Nenhuma dependência nova. Uma única variável principal: contraste do fundo do CTA.

### Métricas anteriores — snapshot de planejamento, não baseline congelado

Período **9–22/out/2026**,14dias completos, fusoSãoPaulo; recalcular pela regra pré-especificada se a publicação ocorrer depois. Essa janela inclui headline anterior em parte, mudança de orçamento e novos anúncios; não é uma coorte homogênea, e essa limitação deve acompanhar o resultado.

| Métrica | Experimental | Controle |
|---|---|---|
| LPV | 7480 | 13292 |
| Leads proxy | 2848 | 5084 |
| CVR | 38,07% | 38,25% |
| Investimento | R$1754,72 | R$2710,93 |
| CPL proxy | R$0,62 | R$0,53 |

Sensibilidade7dias16–22/out:1676/4380=38,26% e2522/6568=38,40%. Primeiro dia completo dos dois anúncios novos22/out tem apenas15LPV; não tratá-lo isoladamente como baseline confiável ou motivo para adiar indefinidamente uma hipótese reversível. Preparação emPR não altera a exposição pública. Registrar essas fases/mix e mudanças futuras, sem atribuir efeitos dos anúncios/orçamentos ao CTA.

### Após publicação

| Métrica | Experimental | Controle |
|---|---|---|
| LPV | Pendente | Pendente |
| Leads proxy | Pendente | Pendente |
| CVR | Pendente | Pendente |
| CPL proxy | Pendente | Pendente |

**Impacto absoluto/relativo:** pendente; nenhuma melhoria medida ou alegada.
**Conclusão:** hipótese implementada e validada tecnicamente; resultado de conversão depende de aprovação/publicação e dados posteriores.
**Aprendizados:** o CTA já estava visível; a mudança corrigiu apenas contraste em ambienteQA, sem mover o botão. Não repetir headline inconclusiva como sucesso.

### QA executada antes de finalizar o PR

- TesteRED falhou na versão anterior, depoisGREEN: guard de duas substituições exatas; scripts, links, conteúdo posterior aoCSS e controle preservados. `git diff --check` limpo.
- NodeVM do script real: **11 verificações aprovadas**, tracking presente/ausente/com erro,delay150ms,modificadores,central/direito/eventocancelado; sem rede nem eventoMeta/joinWhatsApp.
- Chromiumreal:390×844e360×800 capturados e **inspecionados visualmente**. CTA inteiro nas duas primeiras dobras, texto/ícone em duas linhas sem corte; foto e seis benefícios carregados; semoverflow horizontal. Geometria antes/depois idêntica:390x844y503,75–565,75,346×62px;360x800y500,14–560,14,316×60px. Sem nova promessa de oferta/prova social.
- Viewports extras320×740/1280×900,scroll/foco e ativaçãoEnter aprovados; clique físico por coordenada validou uma chamada localLead e timer150ms, URL mantida local. Fallbackhref semJavaScript preservado. DomíniosMeta/WhatsApp bloqueados antes de carregar; timers interceptados sónoQA, nunca noPR. Sem exceçõesJS observadas; isso não é Safari real nem WebVitals de campo.

![CRO-002 — mobile390×844](cro/screenshots/CRO-002-mobile.png)

### Plano de avaliação pré-definido

1. Confirmar SHA publicado e HTML público após aprovação humana; PR/merge sozinho não significa publicação. Congelar **14dias completos imediatamente anteriores ao dia de publicação**, para ambas as campanhas; excluir o dia parcialmente exposto. Guardar revisões de atribuição sem apagar snapshots.
2. Métrica principal estávelLead/LPV;CPLsecundária. Calcular CVRponderada, diferenças absolutas/relativas antes/depois e evolução do controle;IC95% aproximados e sensibilidades7dias, fases de orçamento, anúncios/dispositivos/posicionamentos. Não selecionar janela mais favorável retrospectivamente.
3. Planejamento atualp0=38,07%,MDE+3p.p.,alfa5%bilateral,poder80%: **4170LPV por período**, fórmula de duas proporções independentes. Revalidar uma vez ao congelar o baseline, antes de olhar o desfecho. Não reutilizar4128deCRO-001 como limiar universal. Dados atribuídos/dependentes e tráfego não randomizado limitam poder/causalidade.
4. Checkpoint principal quando atingir a referência de volume **e** cobertura dos dias da semana, examinando consistência/mix. Ritmo7dias atual625,71LPV/dia projeta aproximadamente7dias completos após publicação; não é prazo garantido ou único critério. Monitorar diariamente a integridade, sem declarar vitória pelo primeiro intervalo/p-valor favorável. Não prolongar só para atingir significância; encerrar Inconclusivo se a evidência continuar insuficiente no checkpoint/condições avaliáveis.
5. Se houver mudança externa forte durante a avaliação, preservar endpoint/plano e documentar limitações/sensibilidades; não corrigir Meta ou controlar orçamento por conta própria. Regressão funcional pedePR de correção/reversão, nunca publicação automática.

### Backlog ativo e solicitação de material — não implementar junto ao CRO-002

| Hipótese futura | Evidência atual / próximo trabalho | ICE qualitativo | Dependência |
|---|---|---|---|
| Demonstrar o que chega no grupo com exemplo real | Hoje há promessa genérica e benefícios, mas não exemplo concreto de oferta; testar um exemplo verdadeiro pode reduzir incerteza sobre valor. Não está comprovado que esse seja o motivo de abandono. | I7/C5/E6 | Solicitar3ofertas reais recentes, com data,loja,produto,preço/cupom verificáveis,e1print do conteúdo com nomes/telefones ocultos; validar antes de usar. |
| Confiança verdadeira sem prova social não comprovada | Número16.000/estrelas existentes não foram comprovados. Verificar a alegação e preparar tratamento verdadeiro separado, sem inflar participantes nem criar avaliações. | I6/C6/E8 | Solicitar comprovação do número e autorização de uso; se não houver, propor alternativa sem alegação numérica emPR separado após o teste atual. |

O pedido de materiais será comunicado ao responsável nesta entrega; não é requisito para publicar/avaliar o contraste. Enquanto aguardaPR/dados, avançar pesquisa/copy/plano dessas hipóteses e registrar uma entrega diária útil, não apenas repetir o backlog.

**Artefatos locais:** `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-23/`:rawsMCP/Graph,analysis.json,activities.json,activity-ad-resolution.json,live-validation.json,hypothesis.md,test_scope.py,mobile-qa.json,extra-browser-qa.json,daily-prompt.txt. Evidência de restauração operacional/Telegram será registrada separadamente quando efetivamente confirmada.

### Auditoria operacional complementar — 2026-10-23

Verificação independente do ledger `cron/executions.db` do job714c96de5c45 e dos recibos da ponte: **9 execuções concluídas de14a22/out, com39 mensagens aceitas pelo Telegram** para o destino autorizado. Em22/out os recibos são18710/18711; aceite do transporte não comprova leitura. Houve acompanhamento, mas faltou avanço de hipóteses/insumos; não apresentar a falha atual como uma semana sem executar.

A execução23/out `87a40da3cc1046dbac97f92e2ad9af8c` falhou em12:00:15Z. A ponte marcou `skipped_failed` às12:05:13Z e não emitiu alerta de falha; o job da ponte emsi permanecia saudável. Portanto são dois pontos distintos: recuperar autoridade de execução do perfil e eliminar silêncio de falhas na entrega. O código atual da ponte já mostra um ramo opcional `failure_notices`, mas ativação, deduplicação e envio real ainda não foram verificados nesta auditoria; não declarar recuperação apenas pela existência desse código. Correção com operador @hermes permanece pendente de confirmação. Não copiar tokens nem modificar outros perfis.

## Pesquisa competitiva e roadmap estrutural — 2026-10-23

**Entrega:** [pesquisa completa e plano](cro/research/2026-10-23-competitive-roadmap.md), com cinco concorrentes, inspeção mobile390×844, fontes verificadas, hipóteses, ICE, dependências e plano de avaliação. Benchmark não fornece CVR dos concorrentes nem prova de causalidade; números/descontos/urgência deles não foram validados ou copiados.

**Achados:** ModaPromos mostra mensagens de ofertas com produto/preço/cupom/loja; Só Perfumes e AchadinhoVP tratam objeções perto do CTA; Ninja explica funcionamento e relevância por assunto; Curcio é uma referência adjacente de loja. A ICB já tem CTA na primeira dobra, mas não mostra concretamente o conteúdo recebido. Vídeo do AchadinhoVP não reproduziu na sessão: não foi tratado como exemplo de sucesso ou falha universal.

| Prioridade | Backlog proposto | Gate |
|---|---|---|
| 1 | BL-01: módulo de exemplos reais do que chega no WhatsApp | Ofertas próprias verificáveis, autorização e anonimização |
| 2 | BL-02: reestruturar arquitetura da primeira dobra preservando headline/copy/CTA | Sem material adicional; elegível após CRO-002 |
| 3 | BL-03: contrato de funcionamento e objeções | Confirmar regras reais do grupo |
| 4 | BL-04: demonstrar método/autoria da curadoria | Processo e material real autorizados; um formato por teste |
| Condicional | BL-05: CTA após leitura em versão mais longa | Só se CTA principal realmente sair da tela |

**Decisão:** não implementar nenhum novo tratamento agora. CRO-002 permanece o único experimento emPR; headlineCRO-001 mantida. Priorizar BL-01 após avaliação; se o material estiver pendente, BL-02 evita espera improdutiva. IDsBL são backlog, não novos IDsCRO. Os pedidos de material anteriores continuam válidos, sem nova cobrança repetida.

**Medição futura:** Lead/LPV inalterado, CPL secundário; baseline somente da versão imediatamente anterior, volume/cobertura/mix e intervalos pré-registrados. Referência de planejamento no snapshot7d já coletado:38,26%,MDE3p.p.→4177LPV/período;MDE5p.p.→1516, sem previsão de lift. Regra proposta para testes futuros não altera silenciosamente o plano já registrado doCRO-002. Nenhuma nova coletaMeta ou resultado de conversão nesta pesquisa.

**Operação reconfirmada antes da pesquisa:** gateway ativo atendendo14perfis e ponteTelegramOK em23/out16:35Z; primeiro ciclo completo de análise+envio após correção ainda pendente. Esta pesquisa não reiniciou serviços nem alterou agendamentos.

## Acompanhamento diário — 2026-10-24

**Decisão:** manter CRO-002 **Em PR**, sem novo tratamento enquanto#16 aguarda decisão humana. CRO-001 continua **Inconclusivo**, encerrado no endpoint14–21/out, sem reabrir sua avaliação ou aguardar mais volume. Entrega concreta: [BL-02 — especificação da primeira dobra compacta](cro/research/2026-10-24-first-fold-spec.md), com medidas atuais, intervenção delimitada, riscos, ICE e plano verificável; backlog, não CRO-003.

**Execução/fontes:** início automático09hSãoPaulo; snapshot consolidado2026-10-24T12:02:26Z. Origin/main atualizado e histórico integral lido na main e branch pendente, PRs abertos/fechados consultados; worktree isolada da main48a3628 incorporou a ancestralidade doPR#16. MCP oficial somente leitura, protocolo negociado2025-11-25, schemas/campos e conta consultável confirmados, mesma conversa/sessão; quatro janelas conciliadas exatamente com Graph GET diário29/set–23/out emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente. Contagens de anúncios e breakdowns exatas; resíduo monetário por dispositivo do controle inferior aumcentavo, sem relaxar totais principais. Excluir24/out parcial. **Lead é proxy de clique pré-navegação, não participante confirmado. Baseline histórico36% sem denominador, apenas referência descritiva.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-23–2026-10-23 | Experimental | R$104,28 | 18613 | 534 | 447 | 168 | 37,58% | R$0,62 |
| 1 | 2026-10-23–2026-10-23 | Controle | R$153,65 | 35083 | 822 | 694 | 274 | 39,48% | R$0,56 |
| 3 | 2026-10-21–2026-10-23 | Experimental | R$493,23 | 93967 | 2191 | 1872 | 725 | 38,73% | R$0,68 |
| 3 | 2026-10-21–2026-10-23 | Controle | R$510,00 | 112622 | 2646 | 2261 | 865 | 38,26% | R$0,59 |
| 7 | 2026-10-17–2026-10-23 | Experimental | R$1058,59 | 226578 | 5275 | 4417 | 1674 | 37,90% | R$0,63 |
| 7 | 2026-10-17–2026-10-23 | Controle | R$1309,97 | 314231 | 7322 | 6232 | 2405 | 38,59% | R$0,54 |
| 14 | 2026-10-10–2026-10-23 | Experimental | R$1762,95 | 384989 | 9002 | 7544 | 2886 | 38,26% | R$0,61 |
| 14 | 2026-10-10–2026-10-23 | Controle | R$2721,54 | 682425 | 15652 | 13285 | 5069 | 38,16% | R$0,54 |

**Novidade desde ontem:**23/out experimental168/447=37,58%, contra349/882=39,57% em22/out; controle274/694=39,48%, contra311/826=37,65%. Mudanças diárias−1,99p.p./+1,83p.p.; diferença entre campanhas em23/out−1,90p.p.,IC95% aproximado−7,68a+3,88. Amostras e oscilações não demonstram efeito da landing. Nos7dias, diferença−0,69p.p.,IC95%−2,56a+1,18; Wilson95%experimental36,48–39,34 econtrole37,39–39,81. Semanas não sobrepostas10–16→17–23/out: experimental38,76→37,90% (−0,86p.p./−2,22%relativo),controle37,77→38,59% (+0,82p.p./+2,17%); diferença entre evoluções relativas−4,39pontos percentuais. Comparações observacionais, ICbinomial aproximado para eventos atribuídos/dependentes, sem randomização ou coortes deduplicadas. Não são resultados doCRO-002 não publicado. Nenhuma revisão dos dias já coletados no snapshot23/out; baseline/endpoint fechadoCRO-001 também sem revisão, registros anteriores preservados.

**Mix/fatores externos:** quatro anúncios experimentaisACTIVE eantigoPAUSED; umcontroleACTIVE. União deIDs igual àconsulta anterior, sem adição/remoção. Todos os campos inspecionados de anúncios ativos/conjuntos, copy completa/destinos/UTMs/tracking/atribuição permanecem iguais; única diferença bruta é oURLassinado da miniatura doantigoPAUSED, com mesmoIDcriativo eoutros campos iguais, não nova edição. Orçamentos atuaisACTIVE/R$150exp.eR$170controle, timestamps inalterados; Graph29atividades desde21/out/paginação esgotada, sem nova edição relevante desde aconsulta anterior.23/out é primeiro dia integral após aredução externa docontrole em22/out09:05:28SP; não atribuir variação deentrega aoCTA. Dois anúncios novos somaram7LPV/3Leads/R$1,79 em23/out (1,57%dosLPV), insuficientes para avaliar criativos. Principal404LPV/147Leads, texto4em136/18. Androidsmartphoneexp.117/299=39,13%vscontrole169/420=40,24%;iPhone51/146=34,93%vs104/273=38,10%;sem diagnósticoSafari. Stories137/370=37,03%vs218/560=38,93%,feed23/56vs42/89,Reels8/21vs14/45; não inferir causalidade dos pequenos segmentos.

**Publicação/PRs:**#16 continuaaberto,auto-mergeausente,tratamento sóna branch; Pages`built`para`48a362814fed36b0093e8c4365b9fd39b120fa9a`,updated_at23/out14:47:25Z. Ambas landings públicasHTTP200/byteabyteiguais àmain; cores antigas aindaemprodução. NovoPRoperacional#23 aberto, somentehref/constante do convite emindex3; foi lido integralmente ediffverificado, mas não incorporado/aprovado peloagente. Nãoé outroexperimento nemreseta baseline. Nenhuma data/SHA depublicação doCRO-002 atribuída. Gate é **decisão humana no#16 e confirmaçãoPages+HTML**, não falta deLPV nemmaterial. Após publicação, congelar14dias anteriores e excluir diamixto conformeplanoCRO-002; manter4170LPV como referência deplanejamento original atéa revalidação única prevista, não substituí-la diariamente por outrothreshold.

**Auditoria mobile/entrega concreta:** Chromium390×844e360×800 daprodução, imagensbaseline capturadas einspecionadas:hero248px,foto128px,headlinecomeçaemy299;CTAinteiroemy503,75–565,75e500,14–560,14;gradecomeçaemy732,13e726,52. Semoverflowhorizontal, foto carregada, semexceçãoJS. BL-02 agoratemcandidato específico:compactar apenasmódulomobile,heroalvo136px,foto88px,paddingcontent34px,mesma headline/copy/CTA/cores aprovadas. Meta geométrica éestimativa,não tratamento renderizado; testes deganhos/cortes/identidade pré-definidos.ICEI8/C5/E8; sempromessadelift. BL-01 continua priorizado sechegarem3ofertas reaisautorizadas; pedido23/outpendente, semcobrançarepetida.16.000/estrelascontinuamsemcomprovação. NenhumIDnovo ouHTMLalteradohoje. Guard confirmouquePRdifere damain apenasnasduascoresCSS, scripts/URLs/conteúdo/controle idênticos. NodeVM11verificações aprovadas, comassert deLeadantes denavegação/timer normal; semrede/eventoMeta/joinWhatsApp. Auditoria depadrãoatual,nãoQAdeBL-02 nemnovoSafari/WebVitals.

**Operação separada daentrega:** ledgerconfirma execuçãoautomáticaatual`2e02fa8708ab4115bebbac9b9d8d3f20`,iniciada12:00:24Z eanálise efetivamente realizada, semrepetir afalhapreflightde23/out. Gatewayserve14perfis,heartbeatativo. Pontejob`a37621ef4394`comexecuçãoconcluída12:00:24Z; log identifica`2026-10-23b-failure-notices`/`failure_notices=on`. Isso confirma ativação/execução do ramo, **não envio real dealerta ourecibo desterelatório**: últimaentregaCROregistrada ainda22/out, falha23/outestá`skipped_failed`. Conclusãoatual eentrega posterior dependem doscheduler/ponte apóseste retorno; próximaexecução deve conferirledgercompleted+recibo/destino, semreenviar ambiguamente. Nenhuma credencial, outroperfil, serviço ouagendamentoalterado; nenhumTelegramdireto.

**Próxima observação:**25/out09hSãoPaulo, dados24/outcompleto; checar decisão/publicação#16, eventual rotação#23, atribuição/mix eestado daentrega destaexecução. Não iniciarBL-02 enquanto#16pendente/CRO-002emavaliação. Artefatos atuais em`/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-24/`:rawsMCP/Graph,analysis.json,additional-validation.json,activities.json,live-validation.json,baseline-mobile-audit.json/screenshotsbaseline,operational-probe.json eguard/NodeVM. Reutilização apenasdecódigo, nunca métricas antigascomoatuais. Atualização no mesmoPR#16, semmerge/auto-merge/deploy oualteraçãoMeta/controle/links.

## Acompanhamento diário — 2026-10-25

**Decisão:** manter CRO-002 **Em PR #16, não publicado**, sem outro experimento. CRO-001 permanece **Inconclusivo**, encerrado no endpoint14–21/out, reconsultado sem revisão, não reaberto. **Entrega concreta:** [BL-06 — especificação do rótulo compacto do CTA](cro/research/2026-10-25-cta-copy-spec.md): candidato literal, evidências, riscos de clareza, ICE5/4/9 e gates de teste. Preparação documental, não CRO-003. PrioridadesBL-01/BL-02 preservadas; material solicitado23/out continua pendente, sem cobrança repetida.

**Execução/fontes:** início automático09hSãoPaulo; consolidação2026-10-25T12:03:44Z. Main e histórico completo doPR pendente consultados, PRs abertos/fechados e commits inspecionados; worktree isolada da main`a348725` incorporou a ancestralidade de#16. MCP oficial read-only inicializado, protocolo negociado reutilizado, conta/schema/campos verificados; quatro janelas conciliadas exatamente com Graph GET diário29/set–24/out em investimento,impressões,cliques,LPV,Leads. Aliases selecionados, atribuição unificada preservada, sem paginação/continuações pendentes. Anúncios/breakdowns com contagens e investimento conciliados;25/out incompleto excluído. **Lead=proxy de clique pré-navegação, não entrada confirmada. Baseline histórico36% sem denominador, somente descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-24–2026-10-24 | Experimental | R$84,00 | 14206 | 385 | 325 | 135 | 41,54% | R$0,62 |
| 1 | 2026-10-24–2026-10-24 | Controle | R$165,86 | 38687 | 923 | 783 | 310 | 39,59% | R$0,54 |
| 3 | 2026-10-22–2026-10-24 | Experimental | R$435,58 | 81384 | 1930 | 1654 | 652 | 39,42% | R$0,67 |
| 3 | 2026-10-22–2026-10-24 | Controle | R$506,23 | 112357 | 2703 | 2303 | 895 | 38,86% | R$0,57 |
| 7 | 2026-10-18–2026-10-24 | Experimental | R$1047,47 | 221643 | 5138 | 4307 | 1631 | 37,87% | R$0,64 |
| 7 | 2026-10-18–2026-10-24 | Controle | R$1287,25 | 307927 | 7112 | 6044 | 2334 | 38,62% | R$0,55 |
| 14 | 2026-10-11–2026-10-24 | Experimental | R$1747,09 | 378989 | 8877 | 7422 | 2873 | 38,71% | R$0,61 |
| 14 | 2026-10-11–2026-10-24 | Controle | R$2686,99 | 671175 | 15494 | 13147 | 5047 | 38,39% | R$0,53 |

**Mudança desde ontem/incerteza:**24/out experimental41,54% contra37,58% em23/out (+3,95p.p.), controle39,59% contra39,48% (+0,11p.p.). Diferença diária entre campanhas+1,95p.p.,IC95%aproximado−4,41a+8,31; não demonstra efeito da landing.7d diferença−0,75p.p.,IC95%−2,65a+1,15; Wilson95%experimental36,43–39,33 econtrole37,40–39,85. Semanas não sobrepostas11–17→18–24/out:experimental39,87→37,87% (−2,00p.p./−5,02%relativo),controle38,20→38,62% (+0,42p.p./+1,10%); diferença entre evoluções relativas−6,13pontos percentuais, observacional. Eventos atribuídos/potencialmente dependentes, campanhas não randomizadas e mudanças externas limitam causalidade;14d ainda mistura headlines. **Nenhuma dessas taxas é resultado doCRO-002 não publicado.** Revisão de23/out:experimentalR$104,28→104,29 eimpressões18613→18615;LPV447/Leads168 inalterados. Snapshots anteriores preservados.

**Mix/contexto:** mesma união deIDs, quatro anúncios experimentaisACTIVE eantigoPAUSED, umcontroleACTIVE. Copy completa,destinos,UTMs,tracking,conjuntos eatribuição dosativos iguais àconsulta anterior; única diferença adicional no antigoPAUSED éURLassinado da miniatura, mesmoIDcriativo/demais campos. Orçamento experimentalR$150/controleR$170 eupdated_time iguais;Graph30atividades desde21/out, paginação esgotada, sem nova edição relevante desde ontem. Redução externa do controle22/out09:05:28SP reconfirmada,23–24/out são dois dias completos dessa fase; não atribuir escala/mix aoCTA.24/out principal275LPV/106Leads;texto4em140/25 (62,50%com somente40LPV, não vencedor);novos10LPV/4Leads/R$3,15,3,08%dosLPV. Androidsmartphone88/202=43,56%vs199/479=41,54%;iPhone47/123=38,21%vs111/303=36,63%;sem inferir defeitoSafari. Stories106/267=39,70%vs235/624=37,66%;outros posicionamentos constam nos artefatos, amostras pequenas. LPV/clique/segmentos não sãoWebVitals ou visitas únicas.

**Publicação e integridade do PR:** humano mesclou#23 em24/out14:22:50Z,#25 em25/out03:50:44Z e#26 em25/out03:53:26Z. Diff daslandings contém somentehref/constante dosconvites; headline,estilo,CTA,Pixel/evento ehandler preservados. Pages`built`para`a348725a81cc0569563bed5176d5253a007bef61`,buildconcluído25/out03:54:06Z(00:54:06SP);HTMLpúblico dasduas páginasHTTP200/byteabyteigual àmain. CTApublicado ainda nascoresantigas. Atualização local incorporou **main já aprovada**, sem escolher/trocar convites por iniciativa doagente;controle idêntico àmain ePRdifere emindex3 somente nasduascoresCSS deCRO-002. Manutenção não reinicia baseline. Guarddeescopo eNodeVMsemrede11verificações aprovados,Lead antesdanavegação normal/delay150ms;nenhum eventoMeta real oujoinWhatsApp. Sem novo tratamento visual:equivalência visível àversãoCRO-002jávalidada390×844/360×800 confirmada por escopo exato, não novaQAvisual/Safari/WebVitals.

**Atenção ao responsável ibombonato:**PRoperacional[#24](https://github.com/ibombonato/promos-da-lidi/pull/24) continuaaberto comdestino intitulado“grupo20”, sobrebaseanterior àsrotações23/24. SóURLs, não experimento, mas sua intenção atual precisa ser conferida antes deaprovação para não sobrescrever inadvertidamente arota maisrecente. Não é prova dequeogrupo20 esteja inválido ou cheionem autorização parafechar/mesclar essePR;agente apenasregistrou o conflito potencial. No#16,preservar osconvites atuais euma única hipótese decontraste. Gate doCRO-002 continua **decisão humana no#16 e confirmação depublicaçãoPages+HTML**, nãoLPV oumaterial;após publicação congelar14dias anteriores/excluir diamixto erevalidaruma vez amostra conformeplano. Referênciadeplanejamento original4170mantida atéessegate, semsubstitui-la diariamente.

**Nova preparação:** rótulo atual34caracteres emduaslinhas;canal tambémexplícito nah2/ícone/nomeacessível. CandidatoBL-06 “ENTRAR GRÁTIS NO GRUPO” mantém ação,gratuidade egrupo com22caracteres (−35,29%delcomprimento), sempromessa decomportamentoouganho. Riscoreal deperder clareza sobreWhatsApp,porissoICE5/4/9 eprioridadeinferior àBL-02;preservar aria-label explícito. Reduçãodecaracteres não comprova redução delinhas nemCVR;candidate não renderizado/implementado. Evitar repetirCTAgenérico jácorrigido noPR#3.Nãoalterar headline,CSS,cores,parágrafo eprovasocial junto. Materiais opcionais não bloqueiam testes simples;16.000/estrelas continuamsemcomprovação.

**Operação:** ciclo24/out comprovadamenteconcluído noledger`2e02fa8708ab4115bebbac9b9d8d3f20`às12:13:05Z eentregue pelaponte aodestinoTelegramautorizado às12:15:20Z,recibo`18854`,hash/handlecorrespondentes. Confirma retomadareal apósfalha23/out,nãosóenabled=true;aceite nãocomprovaleiturahumana. Rodadaatual`692dda145a4d4278abc1d33908b8a670`iniciada12:00:54Z;recibodesterelatóriodependedaconclusão posterior. Schedulerativo/pontecomexecuçõesconcluídas,semTelegramdireto,reconfiguração,outrosperfisouagendamentosalterados. Probeagorasepara tabelasexecutions ecron_incidents,evitandoqueumregistrodeincidenteapagueevidênciadeexecução.

**Próxima observação:**26/out09hSãoPaulo, incluindo25/outcompleto;confirmardecisão/publicação#16,rotasoperacionais/mix/revisõeserecibodestaexecução. Artefatosatuais em`/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-25/`:rawsMCP/Graph,analysis.json,additional-validation.json,activities.json,Pages/live,operational-probe.json,guard/NodeVMeverificaçãoremota. Atualização domesmoPR#16;nenhummerge remoto/auto-merge/deploy oualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-10-26

**Decisão:** CRO-002 **Em PR #16, não publicado**; nenhum experimento paralelo. CRO-001 permanece **Inconclusivo**, endpoint14–21/out preservado, reconsultado sem revisão de LPV/Leads/gasto e sem reabrir a avaliação. **Entrega concreta:** [auditoria de preservação de rota e encaminhamento](cro/research/2026-10-26-routing-preservation-audit.md): divergência literal href/constante introduzida externamente, comportamento real reproduzido sem rede e solicitação de confirmação ao responsável ibombonato. Nenhum ID novo ou mudança adicional no tratamento.

**Fontes:** início automático09hSãoPaulo; snapshot consolidado2026-10-26T12:03:42Z. Main atual e histórico integral da branch pendente lidos, PRs abertos/fechados e commits diretos inspecionados; worktree isolada da main`c8a1694` incorporou a ancestralidade de#16. MCP oficial read-only inicializado, protocolo2025-11-25 negociado/reutilizado, schemas/conta consultável/campos confirmados; mesmas conversa/sessão, sem paginação/continuação pendente. Quatro janelas conciliadas exatamente com Graph GET diário29/set–25/out em gasto/impressões/cliques/LPV/Leads. Anúncios/breakdowns reconciliados em contagens e gasto, resíduos monetários de hoje zero. Aliases selecionados, não somados; atribuição unificada preservada.26/out parcial excluído. **Lead=proxy de clique pré-navegação, não entrada confirmada. Baseline histórico36% sem denominador é apenas descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-25–2026-10-25 | Experimental | R$197,89 | 41811 | 952 | 789 | 284 | 35,99% | R$0,70 |
| 1 | 2026-10-25–2026-10-25 | Controle | R$213,22 | 53275 | 1044 | 873 | 346 | 39,63% | R$0,62 |
| 3 | 2026-10-23–2026-10-25 | Experimental | R$386,18 | 74633 | 1871 | 1561 | 587 | 37,60% | R$0,66 |
| 3 | 2026-10-23–2026-10-25 | Controle | R$532,76 | 127048 | 2789 | 2350 | 930 | 39,57% | R$0,57 |
| 7 | 2026-10-19–2026-10-25 | Experimental | R$1074,15 | 223533 | 5208 | 4364 | 1629 | 37,33% | R$0,66 |
| 7 | 2026-10-19–2026-10-25 | Controle | R$1272,25 | 305912 | 6869 | 5821 | 2243 | 38,53% | R$0,57 |
| 14 | 2026-10-12–2026-10-25 | Experimental | R$1831,29 | 397087 | 9308 | 7781 | 2999 | 38,54% | R$0,61 |
| 14 | 2026-10-12–2026-10-25 | Controle | R$2666,73 | 666933 | 15248 | 12940 | 5000 | 38,64% | R$0,53 |

**Mudança desde ontem/incerteza:**25/out experimental35,99% contra41,54% em24/out (−5,54p.p.), controle39,63% contra39,59% (+0,04p.p.). Diferença diária entre campanhas−3,64p.p., IC95%aproximado−8,30a+1,02;7d−1,20p.p.,IC95%−3,11a+0,70. Wilson95%7d experimental35,90–38,77 econtrole37,29–39,79. Semanas não sobrepostas12–18→19–25/out:experimental40,09→37,33% (−2,77p.p./−6,90%relativo),controle38,73→38,53% (−0,19p.p./−0,50%); diferença entre evoluções relativas−6,40pontos percentuais. Eventos atribuídos/dependentes, campanhas distintas, mix/orçamentos e14d ainda parcialmente misto limitam causalidade. **Não são resultados doCRO-002 não publicado nem motivo para reabrirCRO-001.** Revisões24/out:experimentalimpressões14206→14207;controleR$165,86→165,89 eimpressões38687→38690,LPV/Leadsinalterados; snapshots anteriores preservados.

**Mix/contexto:** quatro anúncios experimentaisACTIVE/antigoPAUSED e umcontroleACTIVE; união deIDs sem adição/remoção. Ativos/conjuntos/copy completa/destinos/UTMs/tracking/atribuição idênticos àconsulta anterior; única diferença bruta éURLde miniatura assinada do antigoPAUSED, mesmoIDcriativo/restantes campos. ExperimentalR$150/controleR$170dia eupdated_timeinalterados;31atividadesGraph desde21/out, paginação esgotada, sem nova edição relevante desde ontem. Redução externa docontrole22/out09:05:28SP permanece contexto, não causa comprovada deCVR.25/out principal688LPV/251Leads;texto4em167/19;doisnovos34/14/R$6,71 (4,31%dosLPV),amostra insuficiente paraavaliarcriativos. Android191/517=36,94%vs217/520=41,73%;iPhone93/272=34,19%vs127/350=36,29%;nãoinferirdefeitoSafari. Stories233/682=34,16%vs267/706=37,82%;feed39/78vs64/129,Reels12/29vs15/38,pequenossegmentosnãorandomizados. Sem WebVitals de campo.

**Publicação/integridade:** humano mesclou #27 em25/out19:56:21Z e #28 em26/out02:08:07Z; commits diretos também inspecionados. Pages `built` em `c8a16941814a43a040506a5330903587e5c16852`, concluído26/out02:08:45Z (25/out23:08:45SP); ambas públicas HTTP200/byte a byte iguais à main, cores antigas em produção. Mudanças das duas landings desde ontem são somente URLs; após mascarar exclusivamente convites, HTML inteiro idêntico. Main atual incorporada na branch sem reverter rotas; diff experimental contra main mantém exclusivamente duas cores CSS, controle igual à main. PR#24 operacional antigo ainda aberto, não mesclado/fechado pelo agente. Gate CRO-002: **decisão humana no#16 e confirmação PagesSHA+HTML**, não LPV/material. Após publicação, congelar14dias anteriores, excluir dia misto e revalidar uma vez a amostra conforme plano4170 original, sem novo threshold diário.

**Ressalva nova de QA e encaminhamento:** commit externo `a77f34b` em26/out00:53:18Z (25/out21:53:18SP) deixou href sem query e constante com `?s=cl&p=a&mlu=4&ilr=4`, mesma origem/código de convite. Script reescreve href já ao carregar; semJS usa URL sem query. Guard de escopo CRO-002 PASS, mas exigência antiga de igualdade literal href/constante **FAIL**, reproduzida na fonte publicada e no candidato; **não alegar11passes integrais hoje**. Auditoria comportamental separada em NodeVM:10casos PASS em ambos, Lead antes do timer/navegação normal, delay150ms, tracking ausente/erro e cliques modificados preservados; zero eventos Meta/join. Parâmetros WhatsApp não validados: não é prova de grupo diferente/falha de entrada. **ibombonato: confirmar se a diferença é intencional e qual forma deve permanecer na próxima manutenção; uniformização requer autorização explícita.** Nenhuma URL/parâmetro alterado pelo agente; ressalva não reseta Lead/LPV nem cria espera arbitrária por janela. Sem novo tratamento visual, QA visual não repetida: equivalência ao desenho validado390×844/360×800 é de escopo, não Safari ou validação da rota externa.

**Backlog/entrega:** auditoria operacional com fontes, testes, falha explícita e encaminhamento ao responsável, sem forçar CRO-003. BL-01 com3ofertas reais autorizadas continua prioritário quando houver material; senão BL-02 já especificado (I8/C5/E8), sem implementação antes de avaliar CRO-002. BL-06 alternativa inferior (I5/C4/E9). Pedido de material não repetido;16.000/estrelas seguem sem comprovação.

**Operação:** ciclo25/out `692dda145a4d4278abc1d33908b8a670` concluído12:11:04Z; ponte Telegram registrou envio12:15:51Z, recibo `18927`, handle/hash/execução correspondentes. Aceite não comprova leitura humana. Ciclo hoje `e59b31791c684efe9b3cb16f9ce3e567` iniciado12:00:54Z; envio deste relatório depende da conclusão posterior. Scheduler heartbeat ativo/host serve14perfis; nenhum Telegram direto ou mudança de agendas, credenciais ou outros perfis.

**Próxima observação:**27/out09hSãoPaulo, incluindo26/out completo; decisão/publicação#16, resposta do responsável sobre rota, mix/revisões e recibo deste ciclo. Artefatos em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-26/`: rawsMCP/Graph, analysis.json, additional-validation.json, activities.json, Pages/live, operational-probe.json, cta-production.json, cta-pr.json, strict-source-url-red.log e guard/verificação remota. Nenhum merge remoto/auto-merge/deploy, mutação Meta, alteração de controle, rastreamento ou destino pelo agente.

## Acompanhamento diário — 2026-10-27

**Decisão:** manter CRO-002 **Em PR #16, não publicado**, sem experimento paralelo. CRO-001 continua **Inconclusivo**, endpoint14–21/out preservado e sem revisão de LPV/Leads/gasto; não reaberto. **Entrega concreta:** [BL-02 — plano sensível ao mix](cro/research/2026-10-27-mix-sensitive-first-fold-plan.md), acrescentando decomposição verificável25→26/out e procedimento de padronização por anúncio, cobertura/IDs novos e taxas não estimáveis para o futuro teste. Não muda o plano/4170LPV doCRO-002.

**Fontes:** início automático09hSãoPaulo; snapshot2026-10-27T12:02:39Z. Origin/main atualizado, histórico integral da main e branch pendente lido; PRs abertos/fechados, commits diretos, comentários/reviews consultados (sem resposta nova no#16). Worktree isolada da main`c8a1694` incorporou histórico pendente por fast-forward, sem tocar outras worktrees. MCP oficial somente leitura inicializado, protocolo negociado2025-11-25 reutilizado, conta consultável/schema/campos confirmados; mesma conversa/sessão, sem paginação/continuação pendente. Totais1/3/7/14dias conciliados exatamente com Graph GET diário29/set–26/out em gasto/impressões/cliques/LPV/Leads. Anúncios e breakdowns conciliados, resíduos monetários zero. Aliases selecionados, atribuição unificada preservada;27/out incompleto excluído. **Lead é proxy de clique pré-navegação, não participante confirmado. Baseline histórico36% sem denominador é referência descritiva.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 2026-10-26–2026-10-26 | Experimental | R$126,20 | 30816 | 736 | 597 | 242 | 40,54% | R$0,52 |
| 1 | 2026-10-26–2026-10-26 | Controle | R$135,15 | 38246 | 781 | 662 | 270 | 40,79% | R$0,50 |
| 3 | 2026-10-24–2026-10-26 | Experimental | R$408,09 | 86835 | 2073 | 1711 | 661 | 38,63% | R$0,62 |
| 3 | 2026-10-24–2026-10-26 | Controle | R$514,26 | 130211 | 2748 | 2318 | 926 | 39,95% | R$0,56 |
| 7 | 2026-10-20–2026-10-26 | Experimental | R$1051,61 | 216323 | 5060 | 4244 | 1606 | 37,84% | R$0,65 |
| 7 | 2026-10-20–2026-10-26 | Controle | R$1220,57 | 293926 | 6549 | 5550 | 2157 | 38,86% | R$0,57 |
| 14 | 2026-10-13–2026-10-26 | Experimental | R$1848,29 | 401585 | 9419 | 7845 | 3030 | 38,62% | R$0,61 |
| 14 | 2026-10-13–2026-10-26 | Controle | R$2584,28 | 641236 | 14669 | 12455 | 4842 | 38,88% | R$0,53 |

**Novidade/incerteza:** recuperação experimental35,99→40,54% em25→26/out (+4,54p.p.); controle39,63→40,79%. Diferença entre campanhas26/out−0,25p.p.,IC95%aproximado−5,68a+5,18;7d−1,02p.p.,IC95%−2,97a+0,92. Wilson95%7d experimental36,39–39,31 econtrole37,59–40,15. Semanas não sobrepostas13–19→20–26/out: experimental39,54→37,84% (−1,70p.p./−4,31%relativo),controle38,88→38,86% (−0,02p.p./−0,05%); diferença entre evoluções relativas−4,25pontos percentuais. Observacional, eventos atribuídos/dependentes, sem randomização/coortes deduplicadas;14d inclui13/out parcialmente exposto àheadline. Não são resultados doCRO-002 não publicado. Revisão25/out: somente impressões experimentais41811→41812; demais métricas eendpoint fechado iguais, snapshots preservados.

**Mix e aprendizado concreto:** dois anúncios novos agora105LPV/36Leads/R$17,66,17,59%dosLPV, contra34LPV/14Leads/4,31%em25/out. Principal450/194LPV/Leads, texto4em142/12. Decomposição simétrica da mudança diária+4,54p.p.: parcela aritmética de composição−0,08p.p.; dentro dos anúncios+4,62p.p.; identidade reconciliada sem arredondar antes da soma. Logo não atribuir recuperação simplesmente a maior share dos novos; tampouco isso isola causas dentro dos anúncios ou prevê mix futuro. BL-02 refinado com pesos congelados pré-publicação/IDs comuns/cobertura/novos separados como sensibilidade, primária agregada preservada; mudança futura do módulo mobile eICEI8/C5/E8 mantidos, confiança não inflada. BL-01 continua prioritário se vier material real autorizado; pedido23/out ecomprovação16.000/estrelas pendentes, sem nova cobrança. NenhumIDnovo/HTMLalterado.

**Contexto:** mesma união deIDs, quatro anúncios experimentaisACTIVE/antigoPAUSED e umcontroleACTIVE. Campos dosativos/conjuntos, copy completa/destinos/UTMs/tracking/atribuição idênticos; única diferença bruta no antigoPAUSED éURLda miniatura, mesmoIDcriativo/restantes campos, não nova edição. OrçamentosR$150/R$170dia eupdated_timeinalterados;32atividadesGraph desde21/out/paginação esgotada, nenhuma nova edição relevante desde ontem. Redução externa docontrole22/out09:05:28SP permanece fator externo; não mexer noMeta. Androidexperimental166/385=43,12%;iPhone76/212=35,85%, sem diagnósticoSafari. Distribuição por posicionamento foi coletada/reconciliada nos artefatos; não éWebVitals de campo.

**Publicação/gate/QA:** nenhum novo commit de main desde ontem; Pagesbuilt`c8a16941814a43a040506a5330903587e5c16852`, conclusão26/out02:08:45Z, ambas públicasHTTP200/byteabyteiguais àmain, cores antigas. PR#16aberto/semmerge/auto-merge;#24operacional antigo segueaberto, intenção já encaminhada ao dono. Gate concreto: **ibombonato decidir#16; depois confirmar PagesSHA+HTML e congelar14dias anteriores/excluir dia misto conformeplano**. Não aguardar volume adicional deCRO-001. Ressalva externa dehrefsemquery versusconstanteparametrizada continua: guarddeigualdade literalFAIL preservado na fonte/candidato;10casos comportamentaisNodeVMsemredePASSemambos, Lead antesdotimer/navegação/delay150ms, zeroeventoMeta/join. Parâmetros não validados, sem afirmar grupo diferente/falha nemuniformizarURLsem autorização. GuarddeescopoPASS: somenteduascoresCSS, controle/scripts/links/conteúdo iguaisàmain. Sem nova implementação visual, QA mobile não repetida; equivalência às capturas390×844/360×800 é deescopo,não novoSafari/rotaexterna.

**Operação:** ciclo26/out `e59b31791c684efe9b3cb16f9ce3e567` concluído12:11:41Z e ponte registrou envio12:15:51Z,recibo`18987`,mesmohandle/hash/execução;aceite não comprovaleiturahumana. Incidente23/out consta resolved; hoje execução`f3f50dbf11f2444bb06a72c20ecfde97` iniciada12:00:59Z,análise efetivamente realizada. Schedulerheartbeatativo/hostserve14perfis;entregadehojedependedaconclusão posterior. Duas tentativas iniciais de execuçãoarbitrária/heredocforambloqueadaspelapolíticacron;coleta concluída comhelpersnormaispermitidos,semreconfiguraraprovações. NenhumTelegramdireto, credencial,serviço,outroperfilouagendaalterado.

**Próxima observação:**28/out09hSãoPaulo, incluindo27/outcompleto; decisão/publicação#16,respostaàressalvaderota,mix dosnovoserevisões,recibodeste ciclo. Registro no mesmoPR#16, semPRduplicado/merge/auto-merge/deploy. Artefatos atuais em `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-27/`:rawsMCP/Graph,analysis.json,daily-evidence.json,additional-validation.json,activities.json,Pages/live,operational-probe.json,CTA/guardeverificaçãoremota. Nenhumcontrole,rastreamento,destinoouconfiguraçãoMetaalteradopeloagente.

## Acompanhamento diário — 2026-10-28

**Decisão:** CRO-002 permanece **Em PR #16, não publicado**; nenhum novo experimento. CRO-001 continua **Inconclusivo**, endpoint14–21/out reconsultado sem revisão deLPV/Leads/gasto, sem reabrir sua avaliação. **Entrega concreta:** [BL-06 — viabilidade de renderização do rótulo compacto](cro/research/2026-10-28-cta-copy-render-feasibility.md), comparação exploratória offline, não alteração deindex3 ou novo tratamento. Confirmada uma linha em360/390, mas não em320; benefício geométrico pequeno e risco de clareza preservados, ICE5/4/9 não inflado.

**Fontes:** execução09hSãoPaulo; snapshot2026-10-28T12:02:44Z. Main/histórico completo doPR/PRs abertos e fechados consultados; sem comentários/reviews novos no#16. Worktree isolada, ancestralidade preservada. MCP oficial somente leitura inicializado, protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados. Quatro janelas conciliadas exatamente com GraphGET diário em gasto/impressões/cliques/LPV/Leads; aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente. Anúncios/breakdowns conciliados; resíduo monetário dispositivoexperimentalR$0,000001, demaiszero, totaisprincipaisexatos.28/out parcial excluído. **Lead=proxy pré-navegação, não participante confirmado; baseline histórico36%semdenominador é descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
|1|2026-10-27–2026-10-27|Experimental|R$172,39|40042|873|740|268|36,22%|R$0,64|
|1|2026-10-27–2026-10-27|Controle|R$160,38|39777|897|783|305|38,95%|R$0,53|
|3|2026-10-25–2026-10-27|Experimental|R$496,49|112671|2561|2126|794|37,35%|R$0,63|
|3|2026-10-25–2026-10-27|Controle|R$508,76|131303|2722|2318|921|39,73%|R$0,55|
|7|2026-10-21–2026-10-27|Experimental|R$1073,73|220847|5137|4323|1654|38,26%|R$0,65|
|7|2026-10-21–2026-10-27|Controle|R$1184,65|282615|6291|5362|2096|39,09%|R$0,57|
|14|2026-10-14–2026-10-27|Experimental|R$1928,66|418969|9748|8126|3122|38,42%|R$0,62|
|14|2026-10-14–2026-10-27|Controle|R$2561,48|627699|14381|12248|4782|39,04%|R$0,54|

**Novidade importante — orçamento externo:** GraphGET deatividades confirmou controleR$170→150/dia(**−11,76%**)em **27/out09:47:50SãoPaulo**, transição Processo pendente→Ativa09:48:08; readback atual ambasACTIVE/R$150dia, experimentalinalterada. MCPatividades docontrole retornou vazio, não interpretado comoausência deeditemface daevidênciaGraph;37atividades examinadas,paginaçãoesgotada.27/outé diamixto docontrole;28/outé primeirodia completo, disponível29/out09h. Não atribuir variação deentrega/CVR àlanding nem mudarMeta/baseline/endpoints porcontaprópria. Fasecompleta23–26/out(4dias):controle1200/3012=39,84%,CPLR$0,56,753LPV/dia eR$166,98/dia;experimental829/2158=38,42%,CPLR$0,62,539,50LPV/dia eR$128,10/dia. Não apresentar27/out misto como resultado puro donovo orçamento nem comparar totais4dias com1dia. Após eventualpublicaçãoCRO-002, congelarjanela conforme regra14dias eanotar fases externas/sensibilidades, não selecionar baseline favorável.

**Evolução/incerteza/revisões:**27/out experimental40,54→36,22%(−4,32p.p.) econtrole40,79→38,95%(−1,83p.p.) versus26/out. Diferença diáriaentrecampanhas−2,74p.p.,IC95%aproximado−7,60a+2,13;7d−0,83p.p.,IC95%−2,78a+1,12. Wilson95%7dexperimental36,82–39,72 econtrole37,79–40,40. Semanas nãosobrepostas14–20→21–27/out:experimental38,60→38,26%(−0,34p.p./−0,88%relativo),controle39,01→39,09%(+0,08p.p./+0,21%); diferençaentreevoluçõesrelativas−1,10pontos percentuais.14diasagora sãointeiramente posterioresàheadline, masCRO-001continua encerrado, não reavaliado comendpoint ampliado; janelas gerais não medemCRO-002não publicado. Eventosatribuídos/dependentes,mix/orçamentos ecampanhas distintas limitamICs/causalidade. Revisões26/out:experimentalR$126,20→126,21/impressões30816→30817;controleR$135,15→135,16/impressões38246→38251;LPV/Leadsinalterados,snapshotspreservados.

**Mix:** mesmaunião deIDs, quatroanúncios experimentaisACTIVE/antigoPAUSED eumcontroleACTIVE. Anúnciosativos/conjuntos/copycompleta/destinos/UTMs/tracking/atribuição iguais àconsulta anterior. Única diferença bruta decriativoéURLdinâmica daminiatura doantigoPAUSED,mesmoIDcriativo/restantescampos; separada daediçãoreal deorçamento acima. Novos anúncios186LPV/65Leads/R$43,54 =25,14%dosLPV, contra17,59%em26/out; não repetir participaçãoresidualnem declararvencedores. Principal518LPV/186Leads;texto4em136/17. Android167/427=39,11%vsiPhone101/312=32,37%naexperimental;não édiagnósticoSafari. Posicionamentos/devicecoletados ereconciliados,nãoWebVitalsdecampo.

**Entrega de preparação:** comparação offlinebaselineCRO-002versusmesmodesenho comsórótulo “ENTRAR GRÁTIS NO GRUPO”. Screenshots390×844/360×800capturados einspecionadosvisualmente;2→1linha,altura62→56px/60→56px,topoCTAinalterado503,75/500,14px;em320continuaduaslinhas. Não antecipa significativamente aoferta nemsubstituiBL-02; risco deperder clarezaWhatsAppno textovisível persiste. Headlinecanal,ícone,aria-label,CSS,scripts/convitespreservados;guarddesubstituiçãotextualúnicaPASS. Semoverflowem390/360/320/1280,foto/seisbenefícios,scroll/foco/EntereJSsemexceçõesobservadas;networkMeta/WhatsAppbloqueadoantesdenavegar,timerinterceptadosónoQA,zeroLeadreal/join. Capturasadicionadas aohistóricocomo **pesquisaoffline**,nãoimplementaçãoouSafari real. BL-01comofertasreaisautorizadas eBL-02sem material seguemacima deBL-06;pedidos23/outpendentessemcobrançarepetida,16.000/estrelasnãocomprovados.

**Publicação/gate/QA:** semnovo commitdemaindesdeontem;Pagesbuilt`c8a16941814a43a040506a5330903587e5c16852`,concluído26/out02:08:45Z;ambaspúblicasHTTP200/byteabyteiguaisàmain,coresantigasemprodução. PR#16aberto/semmerge/auto-merge,#24operacionalantigoaberto. Gateespecífico:**ibombonato decidir#16;depoisconfirmarPagesSHA+HTML,congelar14diasanteriores/excluirdiamixto erevalidaruma vezamostraconformeplano4170original**;nãofaltamLPVdoCRO-001nemmaterialparaocontraste. GuarddeescopoPASS:PRindex3apenasduascoresCSS,controle/scripts/URLsigualàmain. Igualdadeliteralhref/constantecontinuaFAILporqueryexterna;10casoscomportamentaisNodeVMPASSemprodução/proposta,semrede. Nãoafirmar11verificaçõesintegralmenteverdes,uniformizarparâmetrossem autorizaçãoouconcluirrotaquebrada. QAexploratóriaBL-06nãoalteraoestadodoPRnemequivaleavalidaçãodeentradaWhatsApp.

**Operação:** ciclo27/out`f3f50dbf11f2444bb06a72c20ecfde97`concluído12:09:14Z;ponteTelegramrecibo`19062`às12:10:50Z,handle/execuçãoeSHA256darespostafinalextraídaconferidos,nãoprovaleiturahumana. Incidente23/outresolved;análisedestaexecução`9024543ca0404410be4c57a10af21d03`efetivamenterealizada,entregadehojedependedaconclusãoposterior. Schedulerhostativo/heartbeatconfirmado;nenhumTelegramdireto,reconfiguração deoutrosperfis/serviços/credenciaisouagendas. execute_codebloqueadopelapolíticacron,semexecução;rotinaconcluídacomhelperspermitidos,semcontornaraprovação.

**Próxima observação:**29/out09hSãoPaulo,incluindo28/outcompleto;decisão/publicação#16,primeirodiaintegraldoorçamentocontroleR$150,mix/revisõese recibodesteciclo. AtualizaçãomesmoPR#16,semPRduplicado/merge/auto-merge/deploy. Artefatosatuaisem`/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-28/`:rawsMCP/Graph,analysis.json,additional-validation.json,activities.json,budget-phases.json,Pages/live,previous-delivery-verified.json,préviaexploratória/capturas/QA,guard/CTAeverificaçãoremota. NenhumHTML,Meta,controle,rastreamentoouconvitealteradopeloagentehoje.

## Acompanhamento diário — 2026-10-29

**Decisão:** manter CRO-002 **Em PR #16, não publicado**, sem outro tratamento. CRO-001 continua **Inconclusivo**, endpoint14–21/out preservado e reconsultado sem revisão de LPV/Leads/gasto. **Entrega concreta de hoje:** [diagnóstico da queda de entrega experimental e encaminhamento ao gestor](cro/research/2026-10-29-experimental-delivery-collapse.md); problema novo a montante da landing, não um experimento ou nova alegação de lift.

**Fontes/integridade:** execução automática09hSãoPaulo, consolidação12:02:31Z. Histórico integral da main e branch pendente/PRs abertos e fechados lido; sem comentários/reviews novos no#16. Worktree isolada da main atual incorporou ancestralidade do histórico pendente. MCP oficial read-only, protocolo2025-11-25 negociado/reutilizado, schemas/conta consultável/campos confirmados;1/3/7/14dias conciliados exatamente com Graph GET diário em gasto/impressões/cliques/LPV/Leads, aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente.29/out parcial excluído das janelas. **Lead=proxy de clique pré-navegação, não entrada confirmada; baseline histórico36% sem denominador apenas descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
|1|2026-10-28–2026-10-28|Experimental|R$2,80|591|16|16|4|25,00%|R$0,70|
|1|2026-10-28–2026-10-28|Controle|R$153,85|36669|855|732|296|40,44%|R$0,52|
|3|2026-10-26–2026-10-28|Experimental|R$301,40|71450|1625|1353|514|37,99%|R$0,59|
|3|2026-10-26–2026-10-28|Controle|R$449,41|114699|2533|2177|871|40,01%|R$0,52|
|7|2026-10-22–2026-10-28|Experimental|R$934,87|194647|4507|3796|1450|38,20%|R$0,64|
|7|2026-10-22–2026-10-28|Controle|R$1168,89|280334|6280|5353|2112|39,45%|R$0,55|
|14|2026-10-15–2026-10-28|Experimental|R$1835,09|396983|9229|7712|2950|38,25%|R$0,62|
|14|2026-10-15–2026-10-28|Controle|R$2523,56|614644|14083|12016|4698|39,10%|R$0,54|

**Alerta novo confirmado:** experimental27→28/out: gasto172,39→2,80 (**−98,38%**), impressões40042→591 (−98,52%), cliques873→16 (−98,17%), LPV740→16 (**−97,84%**); utilização1,87% do orçamento nominal150. Leitura Graph separada somente de entrega e série horária reconfirmam:590impressões/16cliques/R$2,80 entre00h–00h59SP, mais1impressão sem gasto reportado às11h; soma horária exata, não a anomalia antiga de métricas zeradas junto de ações. Controle manteve entrega. Conta ativa/disable_reason0/spend_cap0; campanhas/conjuntos/ativosACTIVE, sem issues/reprovação retornados, estratégiaLOWEST_COST_WITHOUT_CAP. MCPerrors[]/anomaly sem sinal/atividades experimental[] **não excluem problemas de pacing, billing ou restrições não expostas**. Graph37atividades desde21/out/paginação esgotada, nenhuma nova edição relevante depois da mudança conhecida do controle. Causa permanece desconhecida, não culpar landing/Safari/criativo ou afirmar limite interno. Hoje29/out parcial, consulta em torno09h03:experimentalR$9,89/1352impressões/40cliques; há alguma entrega, não recuperação sustentada ou novo dia completo.

**Encaminhamento/ação humana:** ibombonato / gestor autorizado conferir veiculação e histórico no Ads Manager de28/out a partir de00hSP, avisos de revisão/restrição, limites efetivos e cobrança. Se persistir sem causa visível, acionar suporteMeta com IDs/evidências do documento. Pedido de investigação, não chamado já aberto nem autorização de mudar campanha. Sem pausa/ativação/escala/edição pelo agente. GateCRO-002 segue decisão humana no#16 e confirmaçãoPagesSHA+HTML; anomalia exige qualificar a futura avaliação, não excluir dias retrospectivamente ou recalcular checkpoint diariamente. Antiga projeção de prazo por volume deixou de ser utilizável; sem data nova inventada.

**Incerteza/evolução:**4/16 experimental=25%, Wilson95%10,18–49,50, insuficiente para concluir piora da página.7d diferença experimental−controle **−1,26p.p., IC95%−3,28a+0,77**; Wilsonexperimental36,67–39,75/controle38,15–40,77. Semanas15–21→22–28/out:experimental38,30→38,20% (−0,11p.p./−0,28%relativo),controle38,81→39,45% (+0,64p.p./+1,66%); diferença entre evoluções relativas−1,93pontos percentuais. Aproximações para eventos atribuídos/dependentes, campanhas e mix não randomizados, não causalidade nem resultado doCRO-002 ainda não publicado. Revisão27/out controleR$160,38→160,40 e39777→39779impressões; LPV/Leads iguais, snapshots anteriores preservados.

**Controle/orçamento/mix:**28/out primeirodia completoR$150 após redução27/out09:47:50SP. Contra médiasdiárias23–26/out(4dias):LPV753→732 (−2,79%), gasto166,98→153,85 (−7,86%), CVR39,84→40,44% (+0,60p.p.), CPL−6,62%; não comparar total4dias com1dia ou inferir causalidade de uma quarta-feira versussexta–segunda. União deIDs inalterada, quatro ativos experimentais/antigoPAUSED e umcontrole; ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição iguais. Única diferença bruta no antigoPAUSED éminiatura assinada, mesmoIDcriativo/demaiscampos. Novos9LPV/2Leads/R$1,36=56,25% de somente16LPV, não distribuição estável nem validação. Por anúncio/device/placement contagens/gasto conciliados; resíduo monetário posicionamento controleR$0,000001, demaiszero, totais principais exatos.

**Publicação/QA:** main/Pagessemnovo commit `c8a16941814a43a040506a5330903587e5c16852`,built26/out02:08:45Z; ambasHTTP200/HTMLbyteabyteigualàmain, coresantigasemprodução. PR#16aberto/semmerge/auto-merge,#24operacionalantigoaberto, sem nova resposta. GuardPASS:index3apenasduascoresCSS;controle/scripts/links/conteúdopreservados. NodeVM10casoscomportamentaisPASSemprodução/proposta;igualdade literalhref/constanteFAILporqueryexternajáencaminhada, semnormalização/nemprovaderotaquebrada. ZeroeventoMeta/join. Sem implementaçãoHTML/CSShoje:QAvisualmobile não repetida; capturas390×844/360×800anteriores representamodesenhoproposto,não nova auditoriaSafari/WebVitals. BL-01/BL-02/BL-06 e pedidosreais23/outmantidos,semcobrançarepetida.

**Operação separada:** ciclo28/out`9024543ca0404410be4c57a10af21d03`concluído12:12:46Z; ponteTelegramrecibo`19123`às12:15:51Z,handle/execução/hashSHA256daresposta final extraída conferidos. Não prova leitura humana. Jobatual executou análise; recibo dehoje só após conclusão. Schedulerhostativo/heartbeat e próximaexecução30/out12hUTC confirmados. Nenhum envio direto, serviço, credencial, outroperfil ou agendamento alterado.

**Próxima observação:**30/out09hSãoPaulo incluindo29/outcompleto: entregaexperimental/hierarquia/atividades e resposta do gestor, decisão/publicação#16, revisões e recibodesterelatório. Atualizar mesmoPR#16 somente comhistórico/diagnóstico hoje, semnovoCRO/PRduplicado/merge/auto-merge/deploy. Artefatos em`/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-29/`:MCP/Graphatuais,analysis.json,today-validation.json,delivery-probe.json,mcp-delivery-diagnostics.json,delivery-assessment.json,activities.json,Pages/live,NodeVM,previous-delivery-verified.json everificaçãoremota. Nenhuma alteraçãoMeta/controle/rastreamento/destinos/HTML.

## Acompanhamento diário — 2026-10-30

**Decisão:** CRO-002 permanece **Em PR #16, não publicado**; nenhum tratamento paralelo. CRO-001 permanece **Inconclusivo**, endpoint14–21/out reconsultado sem revisão de LPV/Leads/gasto, sem reabrir sua avaliação. **Entrega concreta:** [retomada de entrega e decomposição do mix](cro/research/2026-10-30-delivery-recovery-and-mix.md): primeiro dia completo recuperado confirmado, incidente com causa ainda desconhecida, sensibilidade aritmética por anúncio e encaminhamento atualizado ao gestor.

**Fontes:** execução09hSãoPaulo, snapshot2026-10-30T12:02:27Z. Origin/main atualizado; histórico integral main/PR#16 lido e versão doPR#24 conferida idêntica àmain; PRs abertos/fechados/commits consultados. Worktree isolada da main com ancestralidade pendente preservada. MCP oficial read-only inicializado, protocolo negociado reutilizado, schemas/conta consultável/campos confirmados;1/3/7/14dias conciliados exatamente com GraphGET diário em gasto/impressões/cliques/LPV/Leads, aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente. Anúncios/device/placement conciliados, resíduos monetários zero.30/out parcial excluído das janelas. **Lead=proxy pré-navegação, não participante confirmado; baseline histórico36% sem denominador apenas descritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
|1|2026-10-29–2026-10-29|Experimental|R$171,99|37328|836|711|276|38,82%|R$0,62|
|1|2026-10-29–2026-10-29|Controle|R$140,00|33090|764|662|242|36,56%|R$0,58|
|3|2026-10-27–2026-10-29|Experimental|R$347,18|77961|1725|1467|548|37,36%|R$0,63|
|3|2026-10-27–2026-10-29|Controle|R$454,25|109539|2516|2177|843|38,72%|R$0,54|
|7|2026-10-23–2026-10-29|Experimental|R$859,57|183412|4332|3625|1377|37,99%|R$0,62|
|7|2026-10-23–2026-10-29|Controle|R$1122,17|274838|6086|5189|2043|39,37%|R$0,55|
|14|2026-10-16–2026-10-29|Experimental|R$1915,01|413088|9565|8005|3053|38,14%|R$0,63|
|14|2026-10-16–2026-10-29|Controle|R$2481,41|602391|13769|11757|4565|38,83%|R$0,54|

**Mudança desde ontem — incidente:** após28/outR$2,80/16LPV/4Leads, experimental29/out retomouR$171,99/711LPV/276Leads. Versus27/out, gasto−0,23%,LPV−3,92%; portanto há **um dia completo com entrega retomada**, não somente retomada parcial, nem prova de recuperação sustentada. GraphGET separado de entrega ehorário soma exatamente37328impressões/836cliques/R$171,99 aoMCP; entrega registrada00h e06h–23hSP. Atual30/out~09h: R$34,68/6452impressões/152cliques, parcial. Conta/hierarquia continuam ativas, ambosorçamentosR$150, quatro ativos experimentais/antigoPAUSED, umcontrole; nenhum issue/reprovação retornado. MCPerrors[]/anomalysem sinal não revelam causa. Graph39atividades/paginação esgotada, sem nova edição relevante. **Causa28/out ainda desconhecida:** ibombonato/gestor deve conferir avisos/limites/cobrança daquele período noAdsManager e, se a queda reaparecer sem causa visível, suporteMeta com evidências. Não foi aberto chamado externo, recebida resposta humana ou feita qualquer mutaçãoMeta. Não excluir28/out ou resetar baseline/checkpoint por haver retomada.

**Mix e contribuição analítica:** ad-day27–29/out reconsultado hoje e conciliado exatamente por data/campanha. Novos anúncios29/out318LPV/124Leads/R$75,48=44,73%dosLPV, versus25,14%em27/out; principal 358LPV/141Leads e texto4em1 35LPV/11Leads. CVR27→29/out+2,60p.p. decomposição simétrica **+0,31p.p. composição +2,29p.p. dentro dosanúncios**, identidade exata antes dearredondar. “Dentro” não isola causa nem prova superioridade; não atribuir toda mudança ao mix ou àlanding. Atualização reforça planoBL-02 com primária agregada/pesos pré-congelados/IDs/cobertura/sensibilidade, sem trocar planoCRO-002 ou implementarBL-02. UniãoIDs/ativos/conjuntos/copycompleta/destinos/UTMs/tracking/atribuição inalterados; única diferença bruta éminiatura assinada doantigoPAUSED, mesmoIDcriativo/restantescampos. Materiais reais23/out/comprovação16.000/estrelas continuam pendentes, semcobrançarepetida ou bloqueio indevido decontraste.

**Incerteza/evolução:**29/outCVRexperimental38,82%,Wilson95%35,31–42,45;controle36,56%,Wilson32,97–40,29;diferença+2,26p.p.,IC95%aproximado−2,86a+7,39.7diasdiferença−1,39p.p.,IC95%−3,45a+0,68. Semanas16–22→23–29/out: experimental38,26→37,99% (−0,28p.p./−0,73%relativo),controle38,40→39,37% (+0,97p.p./+2,54%);diferençaentre evoluçõesrelativas−3,26pontos percentuais. Comparações observacionais, eventosatribuídos/dependentes, semrandomização/coorteúnica; não são resultados doCRO-002. Controle23–26/out4diasversus28–29/out2diascompletosdoorçamentonovo:753→697LPV/dia(−7,44%),R$166,98→146,93/dia(−12,01%),CVR39,84→38,59%(−1,25p.p.),CPL−1,87%; usar médiasdiárias enão comparar totais deduraçõesdistintas/atribuircausalidade. Revisão28/outcontrole36669→36670impressões,LPV/Leads/gasto iguais;snapshotspreservados.

**Publicação/gate/QA:** main/Pagessemnovo commit`c8a16941814a43a040506a5330903587e5c16852`,built26/out02:08:45Z;ambosHTMLspúblicosHTTP200/byteabyteiguaisàmain,coresantigasemprodução. #16aberto/semmerge/auto-merge,zero comentários/reviews novos;#24operacionalantigoaberto. **Gate: ibombonato decidir#16; depois confirmarPagesSHA+HTML,congelar14diasanteriores/excluirdiamixto erevalidaruma vez referênciaoriginal4170conformeplano.** Não reaguardarCRO-001 nemreutilizarprojeçãocalendar anterior aoincidente. GuardPASS: apenasduascoresCSS,controle/scripts/URLscopypreservados. NodeVMsemrede10casoscomportamentaisPASSemprodução/proposta;igualdade literalhref/constanteFAILjáencaminhada,semnormalizarquery/alegarrotaquebrada. ZeroeventosMeta/joinWhatsApp. Sem implementaçãohoje,não repetirQAvisualmobile:capturas390×844/360×800doPRsão originais,não novaQA/Safari/WebVitals.

**Operação:** execução29/out`ec63eac070cf4c749dda64f26b7c9162`concluída;ponteTelegramrecibo`19220`às12:10:50Z,handle/execução/SHA256darespostafinalextraída conferidos. Falha23/outnão representa oestado atual. Aceite não comprovaleiturahumana;entrega dehoje dependerá daconclusãoposterior. NenhumTelegramdireto,credencial,outroperfil,serviçoouagendaalterado.

**Próxima observação:**31/out09hSãoPauloincluindo30/outcompleto: persistência daentrega/mix,respostadogestor,decisão/publicação#16,revisõeserecibodesteciclo. Histórico+documentodiagnósticoatualizadosnomesmoPR#16;nenhumnovoCRO/PRduplicado/merge/auto-merge/deployoualteraçãoHTML/controle/rastreamento/destinos. Artefatosatuais em`/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-30/`:rawsMCP/Graph,analysis.json,today-validation.json,delivery-probe.json,mcp-delivery-diagnostics.json,ad-daily-recovery-raw.json,recovery-mix.json,Pages/live,NodeVM,previous-delivery-verified.jsoneverificaçãoremota.

## Acompanhamento diário — 2026-10-31

**Decisão/entrega:** CRO-002 **Em PR #16, não publicado**; CRO-001 continua **Inconclusivo**, endpoint14–21/out e baseline reconsultados sem revisão de LPV/Leads/gasto, sem reabrir. [BL-02 — protótipo exploratório da primeira dobra](cro/research/2026-10-31-first-fold-render-feasibility.md) acrescenta evidência real de renderização: CTA129px mais cedo em390/360/320, dimensões/fontes da oferta intactas; células inteiras de benefícios2→4em390 e0→2em360. Primeira tentativa revelou ornamento invadindoheadline; corrigido sóoffline e capturas finais reinspecionadas. ICEI8/C5/E8 mantido, risco da foto menor explícito; não é lift, implementação ouCRO-003. Gate de desktopbaixo/zoom/reduced-motion permanece antes de qualquer futuro teste. BL-01 segue prioritário se vier material real; pedido23/out/provasocial não comprovada pendentes, sem nova cobrança.

**Fontes:** execução09hSãoPaulo, snapshot2026-10-31T12:02:08Z. Histórico integral da main/branchpendente lido, PRs abertos/fechados/commits consultados; worktree isolada incorporou main atual e ancestralidade#16. MCPoficial somente leitura, protocolo2025-11-25 negociado/reutilizado, schemas/conta/campos confirmados;1/3/7/14dias conciliados exatamente com GraphGET diário emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente; anúncios/device/placement conciliados, resíduos monetárioszero.31/out parcial excluído. **Lead=proxy pré-navegação, não participante confirmado; baseline histórico36%semdenominador é referência descritiva.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
|1|2026-10-30–2026-10-30|Experimental|R$168,30|28204|769|638|225|35,27%|R$0,75|
|1|2026-10-30–2026-10-30|Controle|R$142,35|31993|809|668|252|37,72%|R$0,56|
|3|2026-10-28–2026-10-30|Experimental|R$343,11|66126|1621|1365|505|37,00%|R$0,68|
|3|2026-10-28–2026-10-30|Controle|R$436,20|101753|2428|2062|790|38,31%|R$0,55|
|7|2026-10-24–2026-10-30|Experimental|R$923,60|193004|4567|3816|1434|37,58%|R$0,64|
|7|2026-10-24–2026-10-30|Controle|R$1110,87|271748|6073|5163|2021|39,14%|R$0,55|
|14|2026-10-17–2026-10-30|Experimental|R$1982,20|419584|9842|8233|3108|37,75%|R$0,64|
|14|2026-10-17–2026-10-30|Controle|R$2420,84|585979|13395|11395|4426|38,84%|R$0,55|

**Novidades/limitações:** segundo dia completo de entrega retomada,638LPV/R$168,30 após711LPV em29/out; Graphdelivery-only ehorário conciliam28204impressões/769cliques/R$168,30. Dois dias não demonstram estabilidade prolongada nem causa resolvida doincidente28/out; preservar esse dia emtodasjanelas. Conta/hierarquia ativas eorçamentosR$150/R$150, sem issue/reprovação retornada;40atividadesGraph/paginação esgotada, sem nova edição relevante. Gestoribombonato continua responsável por conferir avisos/limites/cobrança noAdsManager e suporte se recorrência; sem chamado ou resposta inventados.31/out parcialR$31,80/4109impressões/123cliques não entra no desfecho completo.

**CVR/mix:** experimental38,82→35,27%,controle36,56→37,72% em29→30/out. Diferençaentre campanhas30/out−2,46p.p.,IC95%aproximado−7,68a+2,76;7d−1,57p.p.,IC95%−3,60a+0,47. Semanas17–23→24–30/out:experimental37,90→37,58%(−0,32p.p./−0,85%relativo),controle38,59→39,14%(+0,55p.p./+1,43%);diferençaentre evoluçõesrelativas−2,28pontos percentuais. Observacional,eventosatribuídos/dependentes,campanhasnão randomizadas; nenhuma taxa é resultado doCRO-002não publicado. Novos anúncios310LPV/108Leads,48,59%dosLPV; decomposição29→30/out−3,55p.p.=+0,11composição−3,66dentro dosanúncios, aritmética não causal. Androidexperimental167/421=39,67%;iPhone58/217=26,73%, sinal a monitorar semdiagnosticarSafari. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição iguais; diferença bruta apenasminiatura assinada doantigoPAUSED. Controlepré23–26/out4dias versuspós28–30/out3dias:753→687,33LPV/dia,R$166,98→145,40/dia,CVR39,84→38,31%; não comparar totais desiguais/atribuircausalidade. Revisão29/outexperimentalR$171,99→172,01/impressões37328→37331,LPV/Leadsinalterados; snapshotsanteriores preservados.

**Publicação/gate/QA:** humano integrou#29 em30/out16:42:26Z; Pagesbuilt`3df84c5ede7eda8e73d6c167ef4f0e8644eea460`,updated_at16:43:30Z,ambosHTMLsHTTP200/byteabyteiguais àmain. Controle mudou somentehref/constanteexternamente; normalizandoapenasconvites,ambaslandingsiguais àvéspera. Branchincorpora main atual semreverter arota; guardconfirmaindex3apenasduascoresCSS econtroleigualàmain. #16aberto/semmerge/auto-merge,semcomentários/reviews;#24operacionalantigoaberto. **Gate: ibombonato decidir#16; depois confirmarPagesSHA+HTML,congelar14diasanteriores/excluirdiamixto erevalidaruma vezamostra conformeplano4170original.** Não falta volumeCRO-001/material paraocontraste, não iniciarBL-02junto. NodeVM10casoscomportamentaisPASSemprodução/PR/offline;igualdade literalhref/constanteFAILpelaqueryexternajáencaminhada,preservada semnormalização. Chromiumoffline390/360/320/1280,scroll/foco/Entersemexceções,Meta/WhatsAppbloqueadosantesdenavegar,zeroeventoreal/join; nãoSafari/WebVitals. Capturasdehojesão pesquisaoffline,não nova implementação doPR.

**Operação/próximo:**30/out execução`3db003e26abd467793f21a9c1342fdce`concluída12:07:31Z; ponteTelegramrecibo19270às12:10:50Z,execução/handle/hashdarespostafinalextraída conferidos. Falhaantiga23/outnãoéestadoatual; aceite não comprovaleiturahumana. Entregadehojedepende daconclusãoposterior,nenhumenviodireto/reconfiguração/agendaalterada. Próximaobservação01/nov09hSãoPaulo,31/outcompleto: persistênciadeentrega/iPhone/mix,decisão#16,respostadogestor,revisõeserecibo. Atualização somentehistórico/pesquisa/capturasnomesmoPR#16,semCROnovo/HTMLnovo/Meta/controle/rastreamento/destinopeloagente,merge/auto-merge/deploy. Artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-10-31/`:MCP/Graph,analysis.json,today-validation.json,delivery-probe.json,recovery-mix.json,Pages/live,QAoffline,CTAeverificaçãoremota.


## Acompanhamento diário — 2026-11-01

**Decisão:** CRO-002 continua **EmPR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out preservado. Nenhuma alteração de landing ou tratamento paralelo. **Entrega concreta:** [bloqueio GitHub reproduzido e diagnóstico da terceira jornada de retomada](cro/research/2026-11-01-github-auth-blocker-and-delivery-followup.md), com encaminhamento a ibombonato/@hermes. **Atualização desta seção é LOCAL, ainda não enviada aoPR:** credencial dohelper falhouHTTP401Badcredentials noGET/user; leituras públicas continuam possíveis. Não inventar motivo de expiração/revogação. Restaurar autenticação segura e confirmar identidade/permissão antes depush/readback; não foram tentadas escritas remotas após ofail.

Histórico integral main/branchpendente ePRs abertos/fechados lidos; worktreeisolada com main atual ancestral preservado. MCPoficial read-only inicializado/protocolo2025-11-25 negociado e reutilizado; schema/conta consultável/campos verificados, mesma conversa/sessão. Quatrojanelas conciliadas exatamente com GraphGET diário eminvestimento/impressões/cliques/LPV/Leads; aliases selecionados,não somados, sem continuação/paginação pendente. Contagensbreakdowns/ad-dayexatas; resíduosmonetáriosatéR$0,000001, totaisprincipaisexatos.01/novparcialexcluído. **Lead=proxy decliquepré-navegação,não participanteconfirmado;baselinehistórico36%semdenominador édescritivo.**

| Dias | Período inclusivo — São Paulo | Landing | Investimento | Impressões | Cliques link | LPV | Leads proxy | CVR | CPL proxy |
|---|---|---|---|---|---|---|---|---|---|
|1|2026-10-31–2026-10-31|Experimental|R$210,38|27891|879|766|302|39,43%|R$0,70|
|1|2026-10-31–2026-10-31|Controle|R$141,50|31830|767|644|256|39,75%|R$0,55|
|3|2026-10-29–2026-10-31|Experimental|R$550,69|93426|2484|2115|803|37,97%|R$0,69|
|3|2026-10-29–2026-10-31|Controle|R$423,85|96915|2340|1974|750|37,99%|R$0,57|
|7|2026-10-25–2026-10-31|Experimental|R$1049,98|206688|5061|4257|1601|37,61%|R$0,66|
|7|2026-10-25–2026-10-31|Controle|R$1086,48|264890|5917|5024|1967|39,15%|R$0,55|
|14|2026-10-18–2026-10-31|Experimental|R$2097,45|428332|10199|8564|3232|37,74%|R$0,65|
|14|2026-10-18–2026-10-31|Controle|R$2373,76|572820|13029|11068|4301|38,86%|R$0,55|

**Desdeontem:**31/out experimental39,43%versus35,27%em30/out,controle39,75%versus37,72%. Terceirodia completodeentregaretomada:766LPV/R$210,38,conciliaçãohorária/delivery-onlyexata;causa28/outaindadesconhecida,nãoexcluirdia/nemafirmarrecuperaçãodefinitiva. AmbosorçamentosR$150,conta/hierarquiaativas,semnovaediçãorelevanteobservada. Novosanúncios437LPV/160Leads=57,05%dosLPV;decomposição30→31/out+4,16p.p.=-0,35composição+4,51dentro dosanúncios,aritmética,nãocausal. iPhoneexperimental26,73→32,70%(86/263)não mantém magnitude daqueda;controletambémsubiu36,59→37,70%,sem diagnósticoSafari. UniãoIDs,ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoinalterados;únicadiferençabrutaéminiaturaassinadadoantigoPAUSED. Revisão30/outcontroleimpressões31993→31995;LPV/Leads/gastoiguais,snapshotspreservados.

**Incerteza/evolução:**7diasdiferençaexperimental−controle-1,54p.p.,IC95%aproximado-3,53a+0,44.Semanas18–24→25–31/out:experimental37,87→37,61%(-0,26p.p./-0,69%relativo);controle38,62→39,15%(0,54p.p./1,39%);diferençaentreevoluçõesrelativas-2,07pontospercentuais.Observacional,eventosatribuídos/dependentes,campanhasdistintas;nenhumresultadoéefeitodoCRO-002nãopublicado.Experimental7d+1,61p.p.versusreferência36,semtesteestatístico contraela.

**Publicação/gates:** main3df84c5einalterada;Pagesendpointbuildpúblico404,masdeployment7443782385success/Actions41092320136successmaisHTMLHTTP200deambaslandingsbyteabyteiguaisaocommitconfirmamversão. #16aberto,semmerge/auto-merge,zerocomentários/reviews;novo#30operacionalaberto,inspecionado,sóURLsdoinvite.Nãoincorporarconvitependente.Nãoexecutaroutroexperimento.Gatehumano:ibombonatodecidir#16,depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezamostrapelo plano4170original.Gateoperacionalnovo:restaurarGitHubparapublicarregistrodehoje.NãofaltavolumeCRO-001oumaterialparacontraste.GuardduascoresPASS/controleigualàmain;NodeVM10casoscomportamentaisPASS,igualdadeliteralhref/constanteFAILexternapreservada.NovaQAvisualnãorealizada,nãohouveHTML/CSSnovo.ZeroeventoMeta/joinWhatsApp.

**Operação/próximo:**31/outexecuçãof52d10fc04624b98ab4c4d9b0d724ecbcompleted12:11:20Z;ponteTelegramrecibo19335às12:15:51Z/hashdarespostafinalextraídaconferido.Falha23/outnãoéestadoatual;entregadehojesóapósconclusão.Nenhumenviopróprio,agenda/serviço/credencial/outroperfilalterado.Próximaleitura02/nov09hSãoPaulo:01/novcompleto,autenticação/decisão#16,entrega/mix/iPhoneerecibo.Aguardaremotesyncdestediário,semalegarPRatualizado.Artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-11-01/`;semmerge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinos.

## Acompanhamento diário — 2026-11-02

**Decisão:** CRO-002 **Em PR #16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão, não reaberto. **Entrega concreta:** [ressalva de rota resolvida na fonte atual e gates de publicação](cro/research/2026-11-02-route-check-resolved-and-publication-gates.md), com diff verificável, NodeVM e encaminhamento. Registro de01/02-nov **LOCAL, sem sincronização remota**: GETGitHub/user continuaHTTP401/Badcredentials; sem tentar escritas ou inventar causa. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, depois sincronizar documentação preservada. Nenhum novo experimento ou alteração de landing peloagente.

**Fontes:** execução09hSãoPaulo; snapshot final2026-11-02T12:05:09Z. Histórico integralmain/PRpendente e diário local01/nov lidos; PRs abertos/fechados, commits e publicação conferidos. Worktree isolada incorpora main atual e ancestralidade completa pendente. MCPoficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/conta consultável/campos confirmados. Janelas1/3/7/14d conciliadas exatamente comGraphGETdiário emgasto/impressões/cliques/LPV/Leads; anúncios/device/placement ehorário/delivery-onlyexatos, resíduosmonetárioszero. Aliases selecionados, não somados; atribuição unificada preservada, sem páginas/continuações pendentes.02/novparcial excluído. **Lead=proxy pré-navegação, não participante confirmado;baselinehistórico36%semdenominador é descritivo.**

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-01–2026-11-01|Experimental|R$156,48|21739|688|594|244|41,08%|R$0,64|
|1|2026-11-01–2026-11-01|Controle|R$160,16|41335|848|717|274|38,21%|R$0,58|
|3|2026-10-30–2026-11-01|Experimental|R$535,16|77834|2336|1998|771|38,59%|R$0,69|
|3|2026-10-30–2026-11-01|Controle|R$444,01|105160|2424|2029|782|38,54%|R$0,57|
|7|2026-10-26–2026-11-01|Experimental|R$1008,57|186615|4797|4062|1561|38,43%|R$0,65|
|7|2026-10-26–2026-11-01|Controle|R$1033,42|252950|5721|4868|1895|38,93%|R$0,55|
|14|2026-10-19–2026-11-01|Experimental|R$2082,72|410149|10005|8426|3190|37,86%|R$0,65|
|14|2026-10-19–2026-11-01|Controle|R$2305,67|558862|12590|10689|4138|38,71%|R$0,56|

**Desdeontem/incerteza:**01/novexperimental41,08%versus39,43%em31/out(+1,65p.p.),controle38,21%versus39,75%(−1,54p.p.). Diferença diária+2,86p.p.,IC95%aproximado−2,46a+8,18;7d−0,50p.p.,IC95%−2,53a+1,53;Wilson7dexperimental36,95–39,94/controle37,57–40,31. Semanasnão sobrepostas19–25/out→26/out–01/nov:experimental37,33→38,43%(+1,10p.p./+2,95%relativo),controle38,53→38,93%(+0,39p.p./+1,02%);diferençaentre evoluçõesrelativas+1,93pontos percentuais. Experimental7d+2,43p.p.versus36,semtestecontra baseline semdenominador. Comparaçõesobservacionais,eventosatribuídos/dependentes,campanhasdistintas,nãocausalidade,nemresultado doCRO-002nãopublicado.

**Qualidade/revisões:**MCP7d inicial retornou code4/subcode1504022/Too many API requests transitório;retry concluiu. Dentro daexecução,Graphdaily/hourly atualizou impressãoexperimental01/nov21738→21739 enquanto primeira coletaMCP ainda21738:guardexato falhou, snapshotinicial arquivado emsnapshot-120311;MCP1/3/7/14d+série/breakdowns reconsultados, conciliaçãofinalexata. Semrevisão deLPV/Leads/gasto nemdos diascomuns ao snapshot01/nov. Não relaxar contagens/usar dados antigos; preservar ambos snapshots.

**Entrega/mix/contexto:**quarta jornada completa deentregaexperimental desde29/out,594LPV/R$156,48;acumulado29/out–01/nov2709LPV/1047Leads=38,65%,677,25LPV/dia. Causa28/out permanece desconhecida;4dias não comprovam recuperação definitiva, preservar incidente e encaminhamento aogestor AdsManager/suporte serecorrência. Conta/hierarquiaativas/ambosorçamentosR$150,semissue/reprovação retornada;42atividadesGraph/paginaçãoesgotada,semnovaediçãorelevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoiguaisàvéspera;únicadiferençabruta miniaturaassinadadoantigoPAUSED. Quatroativoexperimental/umcontrole;novos346LPV/142Leads/R$83,15=58,25%dosLPV,principal211/88,texto4em137/14. Android190/424=44,81%vsiPhone54/170=31,76%;controle176/424=41,51%/98/292=33,56%;nãoédiagnósticoSafari. Stories184/450=40,89%versus212/562=37,72%;segmentosnão randomizados. Controle23–26/out4diasversus28/out–01/nov5dias:753→684,60LPV/dia(−9,08%),R$166,98→147,57/dia(−11,62%),CVR39,84→38,56%;fases desiguais comparadaspor médiasdiárias,semcausalidade.

**Publicação/QA/gates:**humano integrou#30em01/nov15:43:58Z,somentehref/constanteexperimental;#24fechado semmerge. Pagesdeployment7475240488success01/nov15:44:37Z/Actions41322703411success paraSHA`615605697d2dc6c481094f991591680040649808`;ambaslandingsHTTP200/byteabyteiguais àmain. Coresantigas continuamemprodução,logoCRO-002nãopublicado. Nova rotação remove divergêncialiteralhref/constante: **PASS**,mais10casoscomportamentaisNodeVMPASSemprodução/proposta,Leadpré-navegação/delay150ms/semrede;zeroeventoMeta/join. Nãofoicorreção doagente,nãovalidacapacidade/membresia nemsignificadodosparâmetrosantigos. GuardpropostaPASS: somente2coresCSS,controle/scripts/copy/URLsigualàmainatual. NenhumHTML/CSSnovo,novaQAvisualnão repetida;capturas390/360doPRcontinuamoriginais,nãoSafari/WebVitals. Gateéibombonatodecidir#16aberto/semmerge/auto-merge/semcomentários/reviews;depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. GitHub401éoutrogate para sincronizar documentação,nãofaltamLPVdoCRO-001oumaterialparaocontraste. BL-02preparado permanecefallbacksemimplementarjunto;pedido23/out/ofertasautorizadas/provasocialpendentessemcobrançarepetida.

**Operação/próximo:**01/novexecuçãoe1a4ad60df84469984912508aa23ae41completed12:07:01Z;reciboTelegram19420às12:10:50Z,handle/ID/hashdarespostafinalextraídaconferidos. Incidente23/outresolved,nãoestadoatual. Entregadehojesóapósconclusão;nenhumenviodireto/reconfiguração/agendaalterada. Próximaobservação03/nov09hSãoPaulo,02/novcompleto:autenticação/decisão#16,entrega/mix/revisõese recibo. Histórico/nota preservadosemcommit/patchlocal;nenhumPRatualizadohoje,merge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente. Artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-11-02/`.

## Acompanhamento diário — 2026-11-03

**Decisão:** CRO-002 **Em PR #16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out preservado, reconsultado sem revisão e não reaberto. Nenhum tratamento novo. **Entrega concreta:** [auditoria da mudança externa de prova social e integridade do baseline](cro/research/2026-11-03-visible-proof-change-and-baseline-integrity.md). Commit humano `b657143` mudou16.000→20.000, além de convite; não é manutenção exclusivamente deURL. Data de publicação inferida do deployment7503989616 `success`02/nov21:35:40Z/18:35:40SP, sem presumir exposição individual exata. Dia02/nov é misto; primeiro dia completo do novo conteúdo03/nov, se preservado. Não atribuir a queda diária a essa edição, nem medir CRO-002 antes de publicar. **Novo complemento ao pedido de comprovação:** ibombonato fornecer evidência agregada/datada do20.000, escopo, método de deduplicação/definição de recebimento e autorização, sem nomes/telefones; esclarecer origem das estrelas. Alegação não validada pelo HTML nem pela autoria; não ampliar/reverter por conta própria. Pedido23/out de ofertas reais continua pendente sem cobrança repetida.

**Fontes:** início09hSP; snapshot2026-11-03T12:02:31Z. Main e histórico remoto integral/diário local01–02/nov lidos, PRs abertos/fechados e commits diretos conferidos. Worktree isolada incorporou main22751d4 mais ancestralidade pendente/local, sem apagar registros. MCP oficial read-only: inicialização/protocolo2025-11-25 negociado e reutilizado, schemas/campos/conta consultável confirmados. Quatro janelas conciliadas exatamente comGraphGET diário29/set–02/nov emgasto/impressões/cliques/LPV/Leads, sem paginação/continuação pendente; aliases selecionados, atribuição unificada preservada. Anúncios/breakdowns/entrega horária atual conciliados; resíduos monetárioscontrole porbreakdownR$0,000001, contagens/totaisprincipais exatos.03/nov parcial excluído. **Lead=proxy pré-navegação, não participante confirmado; baseline histórico36% semdenominador somente descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-02–2026-11-02|Experimental|R$184,90|30820|907|766|281|36,68%|R$0,66|
|1|2026-11-02–2026-11-02|Controle|R$179,19|51023|1007|831|317|38,15%|R$0,57|
|3|2026-10-31–2026-11-02|Experimental|R$551,76|80450|2474|2126|827|38,90%|R$0,67|
|3|2026-10-31–2026-11-02|Controle|R$480,86|124190|2623|2192|847|38,64%|R$0,57|
|7|2026-10-27–2026-11-02|Experimental|R$1067,26|186618|4968|4231|1600|37,82%|R$0,67|
|7|2026-10-27–2026-11-02|Controle|R$1077,46|265724|5948|5037|1942|38,55%|R$0,55|
|14|2026-10-20–2026-11-02|Experimental|R$2118,88|402942|10028|8475|3206|37,83%|R$0,66|
|14|2026-10-20–2026-11-02|Controle|R$2298,04|559655|12497|10587|4099|38,72%|R$0,56|

**Desde ontem/incerteza:** CVR experimental41,08→36,68%(−4,39p.p.),controle38,21→38,15%(−0,07p.p.). Diferença02/nov−1,46p.p.,IC95%aproximado−6,21a+3,29;7d−0,74p.p.,IC95%−2,72a+1,25. Wilson7dexperimental36,37–39,29/controle37,22–39,91. Semanas não sobrepostas20–26/out→27/out–02/nov:experimental37,84→37,82%(−0,03p.p./−0,07%relativo),controle38,86→38,55%(−0,31p.p./−0,80%);diferençaentre evoluçõesrelativas+0,73pontos percentuais. Observacional/eventosatribuídos/dependentes/campanhas distintas,não causalidade ou liftCRO-002. Revisão01/novcontroleR$160,16→160,17,impressões41335→41337,cliques848→849;LPV/Leadsiguais,snapshots preservados.

**Entrega/mix:** quinta jornada completa desde29/out:766LPV/R$184,90;acumulado3475LPV/1328Leads=38,22%,695LPV/dia. Não elimina causa desconhecida de28/out;incidente preservado, gestor mantém handoff AdsManager/suporte se recorrência. Conta/hierarquiaativas/ambosorçamentosR$150,semissue/reprovação retornados;44atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição iguais, única diferença bruta miniatura assinada doantigoPAUSED. Novos anúncios agora529LPV/189Leads/R$121,31=69,06%dosLPV;principal208/80,texto4em129/12. Androidexperimental194/503=38,57%,iPhone87/262=33,21%;controle220/548=40,15%/96/281=34,16%;não diagnosticarSafari. Stories206/572=36,01%vs233/623=37,40%;segmentosnão randomizados. Controlepré23–26/out4dias versuspós28/out–02/nov6dias:753→709LPV/dia,R$166,98→152,84/dia,CVR39,84→38,48%;médias diárias, não totais desiguais/causalidade.

**Publicação/QA/gates:** Pagesdeployment7510124905success03/nov04:06:00Z/Actions41576025159success paraSHA`22751d4a722a64c0640538730eeae7e1c1d393c4`;ambosHTMLsHTTP200/byteabyteiguaisàmain. Mudança visível16.000→20.000 separada de rotações deURLs; controle sóURLs por humano. Guard localPASS:candidato versusmainapenasduascoresCSS,controle/scripts/copy/URLspreservados. NodeVMprodução/proposta:igualdade literalhref/constantePASS e10casoscomportamentaisPASS emcada,semrede/Leadreal/join. Chromiumprodução390×844/360×800 capturadoeinspecionadovisualmente:20.000visível,CTAinteiroy503,75–565,75/500,14–560,14,semcorte/overflow/exceçãoJS,fotocarregada/scroll224/276px;Meta/WhatsAppbloqueadosantesdenavegar. Verdeantigo publicado. Capturas são **baseline**,nãoimplementação,nemSafari/WebVitals. Falha inicial de conexãoCDP foi resolvida comChromiumdedicadoXvfb;nenhumpreview emitiuevento.

**Gates concretos:**#16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;APImergeable_stateunknown,nãoafirmarconflito. #31operacionalaberto,sóURL,rota diferente damain:ibombonato conferir intenção antes deaprovar,semmergepeloagente. ibombonato decidir#16;depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. Nova prova social exige marcação/sensibilidade de fases, **não** janela14dias extra ou redefinição seletiva dobaseline. GitHubGET/usercontinuouHTTP401:ibombonato/@hermes restaurar autenticação segura/identidade/permissão;nenhumaescritaremotatentada oucausadeexpiraçãoinventada. Diário01–03/nov/nota dehojepreservadosemcommit/patchlocal;**PRnãoatualizado**. NenhumHTMLnovoouexperimentoCROadicional.

**Operação/próximo:**02/novexecução3eb70ad16ff9433eaa99c43015ac1240completed12:09:19Z;ponteTelegramrecibo19468às12:10:50Z,ID/handle/hashdarespostafinalextraídaconferidos. Falha23/outresolved,nãoestadoatual;entregadehojesóapósconclusão. Semenviopróprio,agendas/serviços/credenciais/outrosperfisalterados. Próximaobservação04/nov09hSP inclui03/novcompleto:primeirodiaintegral20.000,semestimarliftsemamostra/controleadequados,autenticação/decisão#16/respostadaprovasocial/mix/revisõese recibo. Artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-11-03/`;semmerge remoto/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-04

**Decisão:** CRO-002 **Em PR #16, não publicado**; CRO-001 segue **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão e sem reabrir. **Entrega concreta:** [BL-02 — breakpoint mobile-only validado offline](cro/research/2026-11-04-width-only-first-fold-qa.md). O protótipo agora preserva desktop baixo1024×600/1280×720, mantendo avanço129px no mobile. Não é nova implementação/ID ou ganho de conversão. **Histórico01–04/nov ainda LOCAL:** GETGitHub/userHTTP401 persiste; nenhuma escrita remota tentada. ibombonato/@hermes: restaurar autenticação segura e confirmar identidade/permissão para sincronizar documentação; separadamente decidir oPR#16.

**Fontes:** início09hSãoPaulo, snapshot2026-11-04T12:03:01Z. Origin/main atualizado; histórico integralmain/PRs pendentes e diário local lidos, PRs abertos/fechados/commits diretos conferidos. Worktree isolada preserva ancestralidade e todos registros. MCP oficial somente leitura inicializado, protocolo2025-11-25 negociado/reutilizado, schemas/conta/campos confirmados;1/3/7/14dias conciliados exatamente comGraphGETdiário29/set–03/nov emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente. Contagensad/device/placementexatas; único resíduo monetário−R$0,000001 emposicionamentoscontrole, totaisprincipaisexatos. Graphdelivery-only+horário reconcilia o último dia.04/novparcial excluído. **Lead=proxy pré-navegação, não participante confirmado;baselinehistórico36%semdenominador é referência descritiva.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-03–2026-11-03|Experimental|R$157,31|34719|1037|848|268|31,60%|R$0,59|
|1|2026-11-03–2026-11-03|Controle|R$147,15|49936|976|795|276|34,72%|R$0,53|
|3|2026-11-01–2026-11-03|Experimental|R$498,69|87279|2632|2208|793|35,91%|R$0,63|
|3|2026-11-01–2026-11-03|Controle|R$486,52|142299|2832|2343|867|37,00%|R$0,56|
|7|2026-10-28–2026-11-03|Experimental|R$1052,18|181296|5132|4339|1600|36,87%|R$0,66|
|7|2026-10-28–2026-11-03|Controle|R$1064,22|275884|6027|5049|1913|37,89%|R$0,56|
|14|2026-10-21–2026-11-03|Experimental|R$2125,91|402143|10269|8662|3254|37,57%|R$0,65|
|14|2026-10-21–2026-11-03|Controle|R$2248,89|558501|12318|10411|4009|38,51%|R$0,56|

**Novidade/incerteza:** primeiro dia completo após a edição externa16.000→20.000:experimental36,68→31,60%(−5,08p.p.),controle38,15→34,72%(−3,43p.p.). Diferença entre campanhas03/nov−3,11p.p.,IC95%aproximado−7,67a+1,44;7d−1,01p.p.,IC95%−2,98a+0,95. Wilson7dexperimental35,45–38,32/controle36,56–39,24. Semanas21–27/out→28/out–03/nov:experimental38,26→36,87%(−1,39p.p./−3,62%relativo),controle39,09→37,89%(−1,20p.p./−3,07%);diferençaentre evoluçõesrelativas−0,55pontos percentuais. Eventosatribuídos/dependentes,campanhasdistintas,semrandomização;nenhuma dessas taxas medeCRO-002 ainda não publicado. Não culpar a mudança de alegação por um dia com queda nas duas campanhas. Sensibilidade29/out–01/nov versus03/nov, excluindo02/novmisto:exp.1047/2709=38,65%→31,60%;controle1024/2691=38,05%→34,72%;apenasdiagnóstico,não novo baseline ou endpoint. Preservar regra14diaspré-publicaçãoCRO-002, sem espera extra/arbitrária. Revisões02/nov:exp.impressões30820→30821;controleR$179,19→179,20/impressões51023→51026;LPV/Leadsiguais,snapshotspreservados.

**Entrega/mix:** sexta jornada completa desde29/out,848LPV/R$157,31;acumulado4323LPV/1596Leads=36,92%,720,50LPV/dia. Incidente28/out preservado/causa ainda não esclarecida, sem alegar resolução definitiva. Conta/hierarquiaativas,ambosorçamentosR$150,semissue/reprovação retornada;45atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição iguais;únicadiferençabruta miniatura assinada doantigoPAUSED. Novos anúncios:548LPV/149Leads/R$97,48=64,62%dosLPV; principal:261LPV/99Leads; texto4em1:39LPV/20Leads. Decomposição02→03/nov−5,08p.p.=+0,35composição−5,43dentro dosanúncios:identidade aritmética exata,não causal. Androidexperimental188/558=33,69%,iPhone80/289=27,68%;controleAndroid173/490=35,31%;sem diagnósticoSafari. Storiesexperimental223/721=30,93%. Controlepré23–26/out4diasversuspós28/out–03/nov7dias:753→721,29LPV/dia,R$166,98→152,03/dia,CVR39,84→37,89%;médiasdiárias,não totaisdesiguais oucausalidade.

**Pesquisa/QA:** protótipoBL-02acrescenta sóoverrideporlargura;fonteHTMLdoPR intacta.309verificaçõesdeescopo/render/interação passam,desktopbaixo e640×450 idênticos ao baseline;390/360/320semoverflow,CTA129pxmais cedo. Capturas390/360 reinspecionadas peloagenteprincipal,semcolisão/corte;reflow200% foi equivalênciaCSS,nãozoomreal;reduced-motionnone/0sjáexistente preservado. Diagnósticoextra1280×900 tem565pixelsdiferentes nafoto apesar degeometria igual,causa não comprovada. Riscosfotomenor/confiançanãomedidos;ICEI8/C5/E8mantido. Semlift/Safari/WebVitals/conformidadeintegral. Meta/WhatsAppbloqueadosantesdenavegar,interceptaçõessóQA,zeroeventoreal/join;processosdedicadosencerrados. NãoimplementarBL-02junto,nãoatribuirIDnovo;zoomreal/textoampliado ainda gate antesdeeventualimplementação. Materiaisreais23/out ecomprovação20.000/estrelascomplementada03/novseguempendentes,semcobrançarepetida.

**Publicação/gates:** main`22751d4a722a64c0640538730eeae7e1c1d393c4`inalterada;Pagesdeployment7510124905success03/nov04:06:00Z/Actions41576025159success eambosHTMLsHTTP200/byteabyteiguaisàmain. Coresantigasemprodução. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto,sóURL,semdecisão doagente. Fontecandidatalocal atual versusmainapenasduascoresCSS;controle/scripts/copy/convitesiguaisàmain. NodeVMprodução/proposta10casoscomportamentais+igualdadeliteralhref/constantePASSemcada,semrede. Gate:ibombonatodecidir#16,depoisPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. AutenticaçãoGitHub é gate adicional para sincronização: PR não atualizado hoje; a branch remota ainda contém a alegação16.000/convite anterior, enquanto o candidato local preserva20.000 e a rota atual. **Restaurar autenticação e sincronizar com main antes de aprovar oPR**, sem reverter conteúdo humano ou validar a alegação. NenhumPRnovo/merge/auto-merge/deployouHTMLalterado.

**Operação/próximo:** execução03/nov`d4960dfa31934ebeaaab0cd0ed96ea2d`completed;ponteTelegramrecibo19574às12:10:38Z,ID/handle/hashdarespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviodireto. Schedulerhostativo/heartbeat;próximaleitura05/nov09hSPinclui04/novcompleto: verificar se a queda de CVR persiste,efeitosdemix/atribuição,decisão#16/autenticação,retornodaprovasocialerecibodesteciclo. Nenhumaagenda/credencial/serviço/outroperfilalterado. Diário/nota/capturasdepesquisapreservadoslocalmente;artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-11-04/`.

## Acompanhamento diário — 2026-11-05

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão e sem reabrir. [BL-06 — alternativa de CTA preservando WhatsApp](cro/research/2026-11-05-channel-preserving-cta-feasibility.md) refinada com três variantes offline: `ENTRAR GRÁTIS NO WHATSAPP` não reduz linhas/altura mobile; risco de omitir “grupo” registrado, sem promover a hipótese acima deBL-02 nem fabricar benefício geométrico. Sem novo experimento/HTML público. **Histórico01–05/nov LOCAL:** credencialGitHub retornaHTTP401noGET/user, sem tentar escrita; ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão e sincronizar o mesmoPR commain antes de decisão humana. Não alegar atualização remota.

**Fontes:** execução09hSãoPaulo; snapshot2026-11-05T12:03:11Z. Main/histórico completo dosPRs pendentes/diário local lidos, PRs abertos/fechados/commits consultados. Worktreeisolada da main atual incorporou o commitlocal58f0ac9 com todos registros anteriores. MCPoficial somente leitura, protocolo negociado2025-11-25 reutilizado, schemas/campos/conta consultável confirmados. Janelas1/3/7/14dias conciliadas exatamente comGraphGETdiário29/set–04/nov emgasto/impressões/cliques/LPV/Leads; aliases selecionados, atribuição unificada preservada, sem páginas/continuações pendentes. Ad/device/placement eentrega diária/horária conciliados; resíduosmonetárioszero.05/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado. Baseline histórico36% semdenominador é referência descritiva.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-04–2026-11-04|Experimental|R$101,53|16709|557|461|184|39,91%|R$0,55|
|1|2026-11-04–2026-11-04|Controle|R$111,48|27053|629|536|191|35,63%|R$0,58|
|3|2026-11-02–2026-11-04|Experimental|R$443,75|82250|2501|2075|733|35,33%|R$0,61|
|3|2026-11-02–2026-11-04|Controle|R$437,83|128016|2612|2162|784|36,26%|R$0,56|
|7|2026-10-29–2026-11-04|Experimental|R$1150,92|197415|5673|4784|1780|37,21%|R$0,65|
|7|2026-10-29–2026-11-04|Controle|R$1021,85|266268|5801|4853|1808|37,26%|R$0,57|
|14|2026-10-22–2026-11-04|Experimental|R$2085,79|392062|10180|8580|3230|37,65%|R$0,65|
|14|2026-10-22–2026-11-04|Controle|R$2190,74|546603|12081|10206|3920|38,41%|R$0,56|

**Novidades/incerteza:** experimental31,60→39,91%(+8,31p.p.) econtrole34,72→35,63%(+0,92p.p.) em03→04/nov;LPV caíram45,64%/32,58% e gasto35,46%/24,24%. Diferença entre campanhas04/nov+4,28p.p.,IC95%aproximado−1,76a+10,31;7d−0,05p.p.,IC95%−1,98a+1,88;Wilson7dexperimental35,85–38,59/controle35,91–38,63. Recuperação diária não é lift de tratamento não publicado nem resultado causal. Semanas22–28/out→29/out–04/nov:experimental38,20→37,21%(−0,99p.p./−2,59%relativo),controle39,45→37,26%(−2,20p.p./−5,57%);diferença entre evoluçõesrelativas+2,98pontos percentuais, observacional/eventosatribuídos/dependentes/campanhasdistintas. Sensibilidade àalegaçãoexterna:29/out–01/nov versus03–04/nov exclui02/novmisto;experimental1047/2709=38,65%→452/1309=34,53%,controle1024/2691=38,05%→467/1331=35,09%. Não comprova efeito daalegação nemsubstitui baseline14diasdoCRO-002. Revisões03/nov:experimentalR$157,31→157,32/impressões34719→34720;controle49936→49937impressões;LPV/Leadsiguais,snapshotspreservados.

**Entrega/mix:** sete jornadas completas desde29/out,4784LPV/1780Leads=37,21%,683,43LPV/dia; entrega04/nov não repete o quasezero28/out, cuja causa permanece desconhecida/incidente preservado. Conta/hierarquiaativas/ambosorçamentosR$150,semissue/reprovação retornada;46atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição inalterados; única diferença bruta miniaturaassinada doantigoPAUSED. Novos anúncios314LPV/125Leads/R$57,79=68,11%dosLPV;principal128LPV/56Leads,texto4em119/3. Decomposição03→04/nov+8,31p.p.=−0,50composição+8,81dentro dosanúncios, identidade aritmética não causal. Androidexperimental132/313=42,17%,iPhone52/148=35,14%;controle124/320=38,75% e67/216=31,02%,sem diagnósticoSafari. Storiesexperimental152/375=40,53%. Controlepré23–26/out4diasversuspós28/out–04/nov8dias:753→698,13LPV/dia,R$166,98→146,96/dia,CVR39,84→37,67%;médiasdiárias,nãototaisdeduraçõesdistintas/causalidade.

**Pesquisa/QA:** trêsrótulos × quatroviewports390×844/360×800/320×740/1280×900,12combinações reaisChromium. Candidato25caracteres comcanal continua2linhas/62pxem390e2linhas/60pxem360;topo503,75/500,14pxinalterado. Anterior22caracteres semcanal1linha/56pxnessaslarguras,masriscodeclarezapreservado. Novo risco é omitir “grupo”,podendosugerirconversaprivada;semtestedecompreensão/CVR. ICE5/4/9mantido,BL-02acima;nenhumCSSparaforçaroneliner. FontePRintacta/guarddesubstituiçãotextualúnicaPASS. Semoverflow/corte/JSexception,foto/seisbenefícios/scrollnativo/focoTab-Enterpreservados;capturas390/360inspecionadasvisualmente. Primeiroguard falhouporusar substringemvezdelinhacompleta,corrigidoantesdobrowserediagnósticopreservado. Meta/WhatsAppbloqueadosantesdenavegar,interceptaçõessóQA,zeroLeadreal/join;processosdedicadosencerrados,nãoSafari/WebVitals. Pedido23/outdeofertasreais ecomprovação20.000/estrelascomplementada03/novcontinuampendentes,semcobrançarepetida.

**Publicação/gates:** main`22751d4a722a64c0640538730eeae7e1c1d393c4`inalterada;deployment7510124905success03/nov04:06:00Z/Actions41576025159success eambosHTMLsHTTP200/byteabyteiguaisàmain. Verdeantigopublicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto,sóURL. Propostalocal versusmainapenasduascoresCSS;controle/scripts/copy/convitespreservados. NodeVMprodução/proposta10casoscomportamentais+igualdadeliteralhref/constantePASSemcada,semrede. Gatehumano:restaurarGitHub/sincronizar#16comconvite/alegaçãoatualsemvalidá-la,entãodecidir#16;depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezamostrapelo plano4170original. NãoaguardarvolumeCRO-001,nãoabrirPRparalelo/nemalterarMeta.

**Operação/próximo:**04/novexecuçãod15b61f09c084977911bd744bc652046completed12:21:48Z;ponteTelegramrecibo19640às12:25:39Z,ID/handle/hashdarespostafinalextraídaconferidos. Falha23/outresolved,nãoestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat,próximaleitura06/nov09hSPinclui05/novcompleto: verificarvolume/CVR/mix,autenticação/decisão#16,retornosdecomprovaçãoerecibo. Semagenda/credencial/serviço/outroperfilalterado. Diário/nota/capturaspreservadoslocalmenteem`~/work/hermes-scratch/cro-icb-2026-11-05/`,semPRatualizado/merge/auto-merge/deployouHTMLalteradopeloagente.

## Acompanhamento diário — 2026-11-06

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 continua **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão e sem reabrir. [BL-03 — explicação inline da compra, sem desviar o funil](cro/research/2026-11-06-faq-informed-operating-copy-plan.md): evidência nova da FAQ humana publicada, candidato literal, ICE6/5/8, riscos e plano de teste. Não é CRO-003 ou implementação. **Registro01–06/nov ainda LOCAL:** GitHubGET/userHTTP401 persiste; nenhuma escrita remota tentada. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, sincronizar o mesmoPR com main e então decidir#16; branch remota ainda contém16.000/convite anterior. Não aprovar como se estivesse sincronizada.

**Fontes:** início09hSãoPaulo; snapshot2026-11-06T12:02:56Z. Origin/main atualizado; histórico integralmain/PRs pendentes e diário local lidos, PRs abertos/fechados/commits conferidos. Worktree isolada incorporou aa3fd0d preservando registros. MCP oficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados; quatro janelas conciliadas exatamente com GraphGET diário29/set–05/nov emgasto/impressões/cliques/LPV/Leads, aliases selecionados e atribuição unificada preservada, sem páginas/continuações pendentes. Ad/device/placement eentrega diária/horária conciliados, resíduos monetárioszero.06/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado; baseline histórico36% semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-05–2026-11-05|Experimental|R$172,86|28591|879|731|268|36,66%|R$0,65|
|1|2026-11-05–2026-11-05|Controle|R$166,31|38013|845|703|261|37,13%|R$0,64|
|3|2026-11-03–2026-11-05|Experimental|R$431,71|80020|2473|2040|720|35,29%|R$0,60|
|3|2026-11-03–2026-11-05|Controle|R$424,95|115004|2450|2034|728|35,79%|R$0,58|
|7|2026-10-30–2026-11-05|Experimental|R$1151,77|188675|5716|4804|1772|36,89%|R$0,65|
|7|2026-10-30–2026-11-05|Controle|R$1048,17|271192|5882|4894|1827|37,33%|R$0,57|
|14|2026-10-23–2026-11-05|Experimental|R$2011,36|372090|10048|8429|3149|37,36%|R$0,64|
|14|2026-10-23–2026-11-05|Controle|R$2170,34|546030|11968|10083|3870|38,38%|R$0,56|

**Novidades/incerteza:**05/novexperimental39,91→36,66%(−3,25p.p.),controle35,63→37,13%(+1,49p.p.);LPV+58,57%/+31,16%,gasto+70,26%/+49,18% contra04/nov. Diferença diária entrecampanhas−0,46p.p.,IC95%aproximado−5,46a+4,53;7d−0,45p.p.,IC95%−2,37a+1,48. Wilson7dexperimental35,53–38,26/controle35,99–38,70. Semanas23–29/out→30/out–05/nov:experimental37,99→36,89%(−1,10p.p./−2,90%relativo),controle39,37→37,33%(−2,04p.p./−5,18%);diferença entre evoluçõesrelativas+2,29pontos percentuais. Observacional/eventosatribuídos/dependentes/campanhasdistintas,semcausalidade ou lift deCRO-002não publicado. Sensibilidade àalegaçãoexterna29/out–01/nov→03–05/nov,excluindo02/novmisto:experimental1047/2709=38,65%→720/2040=35,29%;controle1024/2691=38,05%→728/2034=35,79%. Não substitui regra14diasdoCRO-002 nem prova efeito daalegação. Revisão04/novcontrole:R$111,48→111,49,impressões27053→27054;LPV/Leadsiguais,snapshotspreservados.

**Entrega/mix:** oito jornadas completas desde29/out,5515LPV/2048Leads=37,14%,689,38LPV/dia;05/novnão repete quasezero28/out,causa aindadesconhecida/incidente preservado. Conta/hierarquiaativas,ambosorçamentosR$150,semissue/reprovação retornada;47atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoiguais;únicadiferençabruta miniaturaassinada doantigoPAUSED. Novosanúncios540LPV/189Leads/R$116,16=73,87%dosLPV;principal168LPV/67Leads,texto4em123/12. Decomposição04→05/nov−3,25p.p.=−0,18composição−3,07dentro dosanúncios,aritmética nãocausal. Androidexperimental173/454=38,11%,iPhone95/277=34,30%;controle151/392=38,52%/108/309=34,95%;sem diagnósticoSafari. Storiesexperimental213/599=35,56%. Controlepré23–26/out4diasversuspós28/out–05/nov9dias:753→698,67LPV/dia,R$166,98→149,11/dia,CVR39,84→37,61%;médiasdiárias,não totaisdesiguais/causalidade.

**Publicação/pesquisa:** humanos integraram#32/#33,mainagora`21c6f1d608c0a9aac84edb83402c28742a53acad`,deployment7592311961success06/nov04:23:54Z/Actions42162192857success;ambosHTMLsHTTP200/byteabyteiguaisàmain eàvéspera. Mudanças somenteFAQ/recurso,não tratamentoICB. FAQindependenteHTTP200/byteabyteigual,12perguntas;fonteexplica indicação versuscompra eafirma quempublica,semverificaçãoindependentedaspermissões dosgrupos. **Atenção:**FAQusaoutroPixel1007235838588459/eventoFAQGrupoClick e sorteio dedoisconvites;index3nãoaalinka. Não adicionaratalhoparaela nemcopiarrastreamento/rotas:alterariafunilforadoescopo. BL-03agoraespecifica apenasmóduloinlineapósCTA: “Como funciona a compra? Você recebe ofertas e cupons no grupo. Se quiser comprar, abre o link da oferta e faz o pedido na loja.” Hipótese de reduzirincerteza,riscodeadiantarcompromissodecompra explícito;semclaimadministrativo oumaterialopcional,ICE6/5/8 eprioridade abaixoBL-01/BL-02mantidos. Testefuturocomúnicomódulo,referência/volumepróprios,QA390/360ehandlerpreservado. Sódocumentaçãohoje,semrenderizarcandidato/novaQAvisualouSafari/WebVitals. Pedidos23/out/comprovação20.000/estrelas03/novcontinuampendentes,semnovacobrança.

**Gates/QA:**#16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto,sóURL. Coresantigaspublicadas. Propostalocal versusmainapenasduascoresCSS;controle/scripts/copy/convitespreservados. NodeVMprodução/proposta10casoscomportamentais+igualdadeliteralhref/constantePASSemcada,semrede/eventoMeta/join. Guardinicialdepreparaçãofalhouporcompararcandidatoàscoresdaprodução; corrigidoparaesperarexatamenteasduascoresjápropostas,semalterarHTMLourelaxarescopo. GateérestaurarGitHub/sincronizar#16,decisãohumana,entãoPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano; nãofaltamLPVdoCRO-001oumaterialparacontraste. NenhumPRnovo,alteraçãoMeta,controle,rastreamento,destino,FAQouHTMLhoje.

**Operação/próximo:**05/novexecução19c7b3c672a34658b87680e6d9d8fd45completed,ponteTelegramrecibo19708às12:15:39Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat;próximaleitura07/nov09hSPinclui06/novcompleto:autenticação/sincronização/decisão#16,volume/CVR/mix eeventualrespostadecomprovação,recibodesteciclo. Nenhumaagenda,serviço,credencialououtroperfilalterado. Diário/notapreservadoslocalmenteem`~/work/hermes-scratch/cro-icb-2026-11-06/`;PRnãoatualizado,semmerge/auto-merge/deploy.


## Acompanhamento diário — 2026-11-07

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 continua **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão e sem reabrir. [Diagnóstico de rascunhos versus configuração live e queda por anúncio](cro/research/2026-11-07-staged-vs-live-and-mix-diagnostic.md): três rascunhos históricos lidos, dois vinculados à experimental; nenhum tratado como edição publicada ou causa da queda. **Histórico01–07/nov ainda LOCAL:** GETGitHub/userHTTP401/Badcredentials reproduzido, sem tentar escrita. ibombonato/@hermes deve restaurar autenticação segura, confirmar identidade/permissão, sincronizar o mesmoPR com main e então decidir#16. A branch remota ainda contém16.000/convite anterior; não aprovar como se atualizada.

**Fontes:** execução09hSãoPaulo; snapshot2026-11-07T12:03:39Z. Origin/main/histórico integralmain/PRs pendentes/diário local consultados, PRs abertos/fechados/commits conferidos. Worktree isolada preservou commitlocal2bb2676 e todos registros. MCPoficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados. Guard inicial parou emnext_actions; continuação draft verificada pelo schema/executada na mesma sessão/conversa, sem publicação/ativação. Quatro janelas e baseline conciliados exatamente comGraphGET diário29/set–06/nov emgasto/impressões/cliques/LPV/Leads; aliases selecionados, atribuição unificada preservada, paginação/continuações esgotadas. Ad/device/placement eentrega diária/horária conciliados, resíduosmonetárioszero.07/novparcial excluído. **Lead=proxy pré-navegação,não participante confirmado;baselinehistórico36%semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-06–2026-11-06|Experimental|R$130,22|20919|597|509|165|32,42%|R$0,79|
|1|2026-11-06–2026-11-06|Controle|R$134,28|27608|665|551|210|38,11%|R$0,64|
|3|2026-11-04–2026-11-06|Experimental|R$404,61|66220|2033|1701|617|36,27%|R$0,66|
|3|2026-11-04–2026-11-06|Controle|R$412,09|92676|2139|1790|662|36,98%|R$0,62|
|7|2026-10-31–2026-11-06|Experimental|R$1113,69|181391|5544|4675|1712|36,62%|R$0,65|
|7|2026-10-31–2026-11-06|Controle|R$1040,11|266806|5738|4777|1785|37,37%|R$0,58|
|14|2026-10-24–2026-11-06|Experimental|R$2037,29|374395|10111|8491|3146|37,05%|R$0,65|
|14|2026-10-24–2026-11-06|Controle|R$2150,98|538556|11811|9940|3806|38,29%|R$0,57|

**Novidades/incerteza:**06/novexperimental36,66→32,42%(−4,25p.p.),controle37,13→38,11%(+0,99p.p.);LPV−30,37%/−21,62%,gasto−24,67%/−19,26% contra05/nov. Diferença diária−5,70p.p.,IC95%aproximado−11,44a+0,05;7d−0,75p.p.,IC95%−2,69a+1,20;Wilson7dexperimental35,25–38,01/controle36,01–38,75. Semanas24–30/out→31/out–06/nov:experimental37,58→36,62%(−0,96p.p./−2,55%relativo),controle39,14→37,37%(−1,78p.p./−4,54%);diferençaentre evoluçõesrelativas+1,99pontos percentuais. Observacional/eventosatribuídos/dependentes/campanhasdistintas; não causalidade ou liftCRO-002não publicado. Revisão05/nov:exp.impressões28591→28592;controleR$166,31→166,32/impressões38013→38014;LPV/Leadsiguais,snapshots preservados.

**Entrega/mix/rascunhos:** nove jornadas completas desde29/out,6024LPV/2213Leads=36,74%;06/novnão repete quasezero28/out,causa original ainda desconhecida/incidente preservado. Conta/hierarquiaativas/ambosorçamentosR$150,semissue/reprovação retornada;48atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoiguais;únicadiferençabruta miniaturaassinada doantigoPAUSED. Dois anúncios lançados21/out agora394LPV/120Leads=77,41%dosLPV,CVR30,46%,contra35,00%em05/nov;estabelecidos45/115=39,13%. Sériead-day30/out–06/nov reconsultada/conciliada por dia;decomposição05→06/nov−4,25p.p.=−0,33composição−3,92dentro dosanúncios,aritmética nãocausal. Androidexp.113/322=35,09%,iPhone51/186=27,42%;não diagnosticarSafari. Rascunho do conjuntoexp.atualizado07/ago sugere22–45,masliveé24–50/mobile/AdvantageAudience0;rascunho doanúncio de21/out altera metadadoscriativos cuja publicação não foi comprovada;terceiro é outra campanha,fora doescopo. Não tratar descoberta como mudança dehoje;gestor deve confrontar pendências comlive antes dequalquer publicação manual,sempublicarem lote. Nenhuma mutaçãoMeta solicitada/executada.

**Publicação/QA/gates:** main`21c6f1d608c0a9aac84edb83402c28742a53acad`inalterada;deployment7592311961success/Actions42162192857success eambosHTMLsHTTP200/byteabyteiguaisàmain;verdeantigo publicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto,sóURL. Fontecandidatalocal versusmainapenasduascoresCSS,controle/scripts/copy/convitespreservados;NodeVMprodução/proposta10casoscomportamentais+igualdadeliteralhref/constantePASSemcada,semrede/eventoMeta/join. NenhumHTML/CSSnovo,novaQAvisualnão repetida. GateérestaurarGitHub/sincronizar#16,decisãohumana,depoisPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. Rascunhos não criam janelaextra,nãofaltamLPVdoCRO-001oumaterialparacontraste. BL-02ICE8/5/8 seguefallbacksem material,comsensibilidade de mix pré-fixada;BL-03inlineeBL-06comriscos mantidos,semimplementarjunto. Pedidos23/out/comprovação20.000/estrelas03/novcontinuampendentes,semnovacobrança.

**Operação/próximo:**06/novexecução0376b2ea66e04f7db4d34befd85b57ffcompleted12:07:41Z;ponteTelegramrecibo19756às12:10:38Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Jobatualb824df4990f74eb695b38f1e5d1e1378executou análise. Próximaobservação08/nov09hSPinclui07/novcompleto: verificar persistência daqueda e mix,autenticação/sincronização/decisão#16,eventualrespostadecomprovaçãoerecibo. Semagenda/serviço/credencial/outroperfilalterado. Histórico/nota preservados emcommit/patchlocal,artefatos`~/work/hermes-scratch/cro-icb-2026-11-07/`;PRnãoatualizado,semmerge/auto-merge/deploy.

## Acompanhamento diário — 2026-11-08

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão e sem reabrir. [BL-03 — viabilidade da explicação inline e custo de atenção](cro/research/2026-11-08-inline-operating-copy-render-feasibility.md): candidato executado exclusivamente offline, mantendo CTA e acrescentando explicação do funcionamento. Cabe após o botão no mobile, mas desloca a grade91,31px; não alegar ganho geométrico/compreensão/CVR. ICE6/5/8 e prioridade abaixoBL-02 preservados. Nenhum novo experimento/ID ou alteração de landing.

**Fontes:** execução09hSãoPaulo; métricas consolidadas2026-11-08T12:03:14Z. Origin/main atualizado, históricos integrais main/PRs pendentes/diário local lidos; PRs abertos/fechados e commits diretos conferidos. Worktree isolada incorporou main atual e commitlocal359c056 preservando todos os registros. MCPoficial somente leitura inicializado, protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados; quatro janelas conciliadas exatamente comGraphGET diário29/set–07/nov emgasto/impressões/cliques/LPV/Leads, aliases selecionados, atribuição unificada preservada, paginação/continuações verificadas. Ad/device/placement eentrega diária/horária conciliados; resíduo monetário de dispositivo do controleR$0,000001, demaiszero, contagens/totaisprincipaisexatos.08/novparcial excluído. **Lead=proxy pré-navegação, não participante confirmado; baseline histórico36% semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-07–2026-11-07|Experimental|R$146,63|22236|746|611|196|32,08%|R$0,75|
|1|2026-11-07–2026-11-07|Controle|R$151,36|28962|698|582|225|38,66%|R$0,67|
|3|2026-11-05–2026-11-07|Experimental|R$449,71|71749|2222|1851|629|33,98%|R$0,71|
|3|2026-11-05–2026-11-07|Controle|R$451,96|94587|2208|1836|696|37,91%|R$0,65|
|7|2026-11-01–2026-11-07|Experimental|R$1049,94|175738|5411|4520|1606|35,53%|R$0,65|
|7|2026-11-01–2026-11-07|Controle|R$1049,97|263941|5669|4715|1754|37,20%|R$0,60|
|14|2026-10-25–2026-11-07|Experimental|R$2099,92|382426|10472|8777|3207|36,54%|R$0,65|
|14|2026-10-25–2026-11-07|Controle|R$2136,45|528831|11586|9739|3721|38,21%|R$0,57|

**Novidade/incerteza:** experimental32,42→32,08%(−0,34p.p.),controle38,11→38,66%(+0,55p.p.) em06→07/nov;LPV+20,04%/+5,63%,gasto+12,60%/+12,72%. Diferença diária−6,58p.p.,IC95%nominal aproximado−12,00a−1,16;3d−3,93p.p.,IC95%−7,02a−0,83;7d−1,67p.p.,IC95%−3,63a+0,29. Intervalos diários/3d que excluemzero não demonstram efeito causal da landing ou autorizam escolher endpoint favorável: campanhasdistintas,eventosatribuídos/dependentes,múltiplasleituras/mix. Wilson7dexperimental34,15–36,94/controle35,83–38,59. Semanas25–31/out→01–07/nov:experimental37,61→35,53%(−2,08p.p./−5,52%relativo),controle39,15→37,20%(−1,95p.p./−4,98%);diferença entre evoluçõesrelativas−0,54pontos percentuais. Ambas caíram na semana; não medirCRO-002 antes de publicar nem reabrirCRO-001. Revisões06/nov:impressõesexperimental20919→20921/controle27608→27611;LPV/Leads/gasto iguais,snapshots preservados.

**Entrega/mix/contexto:** décima jornada completa desde29/out,6635LPV/2409Leads=36,31%;07/nov611LPV/R$146,63 não repete quasezero28/out, cuja causa permanece desconhecida/incidente preservado. Conta/hierarquiaativas/ambosorçamentosR$150,semissue/reprovação retornada;51atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoiguais;únicadiferençabruta miniaturaassinada doantigoPAUSED. Novosanúncios490LPV/155Leads/R$110,77=80,20%dosLPV;principal87/32,texto4em134/9. Androidexperimental126/381=33,07%,iPhone70/230=30,43%;Stories152/484=31,40%,sem diagnósticoSafari oucausalidade porsegmento. Controlepré23–26/out4diasversuspós28/out–07/nov11dias:753→674,64LPV/dia,R$166,98→147,97/dia,CVR39,84→37,73%;médiasdiárias,nãototaisdeduraçõesdistintas.

**Pesquisa/QA offline:** oito combinaçõesbaseline/candidato em390×844/360×800/320×740/1280×900; screenshotsmobilecapturados e inspecionadosvisualmente. Apenas inserção deumparágrafousandoCSSexistente; guardRED/GREEN e reconstruçãointegralPASS, scripts/links/CTA/aria preservados. CTA continuaem503,75–565,75/500,14–560,14px;explicação79,31px nosdoismobiles;grade732,13→823,44/726,52→817,83px,estaúltima começa fora dadobra. Custo deatenção real explicitado, semcombinarcompactaçãoBL-02. Semoverflow/cortes/exceçãoJS, foto/seisbenefícios/scrollnativo/focoTab-Enterpreservados. NodeVMoffline10casos+igualdadeliteralhref/constantePASS;Meta/WhatsAppbloqueadosantesdenavegar/interceptaçõessóQA/zeroLeadreal/join. Fonte da landing na branch intacta;capturas são pesquisa, nãoimplementação/Safari/WebVitals. Textoampliado/desktopbaixo/compreensão ainda gates deeventualtestefuturo. Pedidos23/outdeofertasreais ecomprovação20.000/estrelas03/novcontinuampendentes,semnovacobrança.

**Publicação/gates:** humano integrou#34;main`3c93fbe7d7263d6b47cdfa2f0523f8e1c79602cc`,deployment7630609976success08/nov03:05:41Z/Actions42441187719success;ambosHTMLsHTTP200/byteabyteiguaisàmain. Controle mudou somentehref/constante porhumano,experimentalintacta;rotasoperacionaispreservadas,nãoresetambaseline. Endpoint de statuses retornouHTTP504em tentativasiniciais;GETcomper_page100 recuperou evidênciadoSHAexato,sem presumirpublicação antesdoreadback. Verdeantigo seguepublicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto,sóURL. Propostalocal versusmainapenasduascoresCSS,controle/scripts/copy/convitespreservados;NodeVMprodução/proposta10casos+igualdadehref/constantePASSemcada. **GitHubGET/userHTTP401/Badcredentials persiste:** nenhumaescritaremotatentada;histórico01–08/novLOCAL. ibombonato/@hermes:restaurar autenticaçãosegura/identidade/permissão,sincronizar#16commainatual/todohistórico eentãodecidir;branchremotaaindacontém16.000/conviteanterior,nãoaprovar comoseatualizada. Depois deaprovação,confirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste.

**Operação/próximo:**07/novexecuçãob824df4990f74eb695b38f1e5d1e1378completed;ponteTelegramrecibo19815às12:10:38Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat epróximaexecução09/nov12hUTCconfirmados,semalteraçãoagenda/serviço/credencial/outroperfil. Próximaobservação09/nov09hSPinclui08/novcompleto:quedaCVR/mix,autenticação/sincronização/decisão#16,retornodecomprovaçãoerecibo. Diário/pesquisa/capturaspreservadosemcommit/patchlocalem`~/work/hermes-scratch/cro-icb-2026-11-08/`;PRnãoatualizado,semmerge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-09

**Estado vigente/decisão:** CRO-002 **Em PR #16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão, sem reabrir. **Entrega concreta:** [BL-02 — sensibilidade por anúncio/dispositivo em fins de semana comparáveis](cro/research/2026-11-09-weekend-mix-and-next-test-sensitivity.md): diagnóstico novo e refinamento explícito do próximo plano, não CRO-003 ou mudança na landing. **Histórico01–09/nov continua LOCAL:** GitHubGET/userHTTP401Badcredentials; nenhuma escrita remota tentada. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, sincronizar o mesmoPR com main/todo histórico e só então decidir#16; branch remota ainda contém16.000/convite anterior.

**Fontes:** execução09hSãoPaulo; métricas principais consolidadas2026-11-09T12:02:46Z. Origin/main atualizado; históricos integrais main/PRs pendentes/diário local, PRs abertos/fechados/commits consultados. Worktree isolada preserva1690518 e todos registros. MCPoficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados;1/3/7/14dias conciliados exatamente comGraphGET diário29/set–08/nov emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, paginação/continuações verificadas. Ad/device/placement eentrega diária/horária conciliados; resíduos monetários dos breakdowns do último diazero.09/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado; baseline histórico36% semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-08–2026-11-08|Experimental|R$174,79|29586|903|756|278|36,77%|R$0,63|
|1|2026-11-08–2026-11-08|Controle|R$174,09|35817|830|702|254|36,18%|R$0,69|
|3|2026-11-06–2026-11-08|Experimental|R$451,64|72745|2246|1876|639|34,06%|R$0,71|
|3|2026-11-06–2026-11-08|Controle|R$459,73|92392|2193|1835|689|37,55%|R$0,67|
|7|2026-11-02–2026-11-08|Experimental|R$1068,25|183587|5626|4682|1640|35,03%|R$0,65|
|7|2026-11-02–2026-11-08|Controle|R$1063,89|258423|5650|4700|1734|36,89%|R$0,61|
|14|2026-10-26–2026-11-08|Experimental|R$2076,82|370202|10423|8744|3201|36,61%|R$0,65|
|14|2026-10-26–2026-11-08|Controle|R$2097,32|511375|11372|9568|3629|37,93%|R$0,58|

**Novidades/incerteza:** experimental32,08→36,77%(+4,69p.p.),controle38,66→36,18%(−2,48p.p.) em07→08/nov;LPV+23,73%/+20,62%,gasto+19,20%/+15,02%. Diferença diária+0,59p.p.,IC95%nominal aproximado−4,35a+5,53;3d−3,49p.p.,IC95%−6,57a−0,40;7d−1,87p.p.,IC95%−3,81a+0,08. Wilson7dexperimental33,67–36,41/controle35,53–38,28. Semanas26/out–01/nov→02–08/nov:experimental38,43→35,03%(−3,40p.p./−8,85%relativo),controle38,93→36,89%(−2,03p.p./−5,23%);diferença entre evoluçõesrelativas−3,63pontos percentuais. Recuperação diária não comprova melhora sustentável;ambas caíram na semana. Eventosatribuídos/dependentes,campanhasdistintas,múltiplasleituras/mix limitamICs/causalidade;nenhuma taxa medeCRO-002não publicado. Revisão07/nov:somenteimpressõesexperimental22236→22238/controle28962→28964;LPV/Leads/gasto iguais,snapshots preservados.

**Entrega analítica:** sériead-day/device-day31/out–08/nov atual reconsultada/conciliada porcampanha/data. Fins de semana iguais31/out–01/nov versus07–08/nov:experimental546/1360=40,15%→474/1367=34,67%;controle530/1361=38,94%→479/1284=37,31%. Experimental−5,47p.p.=−0,29composição−5,18dentro dosanúncios;padronização porpesos anteriores34,56%,queda não desaparece. Smartphoneexperimental1359/1360→1366/1367LPV cobre todosLeads:Android43,84→36,20%,iPhone32,33→32,05%; não sustenta culpabilizarSafari. Guard inicial detectou célulaother ausente; sensibilidadeexplicitamente restrita aosdoissmartphones comcobertura,todosraws/totaispreservados,semimputarCVRvazia. Decomposições marginais não somáveis/nãocausais;fimdesemana nãoéendpointnovo ealegaçãosocialexterna mudouentreperíodos. PlanoBL-02 refinado comcobertura/pesospré-fixados poranúncio e smartphones,separados da primáriaagregada;compactaçãoúnica/ICE8/5/8inalterados,semnovogatedeespera. BL-03segueabaixoBL-02comcustodeatenção91px;materiais23/out/comprovação20.000/estrelas03/novpendentes,semnovacobrança.

**Contexto/QA/publicação:**11jornadas completas desde29/out,7391LPV/2687Leads=36,36%;08/novnão repetequasezero28/out,cujacausa permanece desconhecida/incidente preservado. Conta/hierarquiaativas,ambosorçamentosR$150,semissue/reprovação retornada;53atividadesGraph/paginaçãoesgotada,semnovaediçãoMeta relevante. UniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoiguais;únicadiferençabruta miniaturaassinadadoantigoPAUSED. Novosanúncios595LPV/224Leads=78,70%dosLPV;recuperação07→08/nov+4,69p.p.=+0,07composição+4,63dentro dosanúncios,aritmética nãocausal. Maininalterada3c93fbe7d7263d6b47cdfa2f0523f8e1c79602cc;deployment7630609976success/Actions42441187719success eambosHTMLsHTTP200/byteabyteiguaisàmain,verdeantigopublicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto,sóURL. Propostalocal versusmainapenasduascoresCSS;controle/scripts/copy/convitespreservados. NodeVMprodução/proposta10casos+igualdadehref/constantePASSemcada,semrede/Leadreal/join. NenhumHTML/CSSnovo,novaQAvisualmobile não repetida. Gate:restaurarGitHub/sincronizar#16,decisãohumana,depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste.

**Operação/próximo:**08/novexecuçãof58680f45ff846ff88262de500bd0fd6completed12:10:53Z;ponteTelegramrecibo19873às12:15:40Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat epróximaexecução10/nov12hUTCconfirmados,semalteraçãoagenda/serviço/credencial/outroperfil. Próximaobservação10/nov09hSPinclui09/novcompleto: persistênciadarecuperação/mix,CVRsemanal,autenticação/sincronização/decisão#16,retornodecomprovaçãoerecibo. Histórico/pesquisapreservadosemcommit/patchlocalem`~/work/hermes-scratch/cro-icb-2026-11-09/`;PRnãoatualizado,semmerge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-10

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão, não reaberto. [Auditoria do novo clone pausado e rascunho novo no anúncio original](cro/research/2026-11-10-paused-clone-and-new-draft-handoff.md), com encaminhamento ao gestor e refinamento do planoBL-02. Nenhum novo tratamento. **Histórico01–10/nov LOCAL:** GETGitHub/userHTTP401Badcredentials persiste; nenhuma escrita remota tentada. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, sincronizar#16commain/todohistórico e sóentão decidir; branchremotaaindacontém16.000/convite anterior.

**Fontes:** início09hSãoPaulo; snapshot principal2026-11-10T12:03:29Z. Origin/main/históricos integrais main/PRs pendentes/diário local lidos, PRs abertos/fechados e commits consultados. Worktree isolada da mainab142e8 incorporou commitlocale221020 preservando todos registros/rotas atuais. MCPoficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados;1/3/7/14dias conciliados exatamente comGraphGETdiário29/set–09/nov emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, paginação/continuações verificadas. Ad/device/placement eentrega diária/horária conciliados; único resíduo monetário−R$0,000001 emposicionamentoexperimental, contagens/totaisprincipaisexatos.10/novparcial excluído. **Lead=proxy pré-navegação,não participante confirmado;baseline histórico36%semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-09–2026-11-09|Experimental|R$142,87|22509|752|634|225|35,49%|R$0,63|
|1|2026-11-09–2026-11-09|Controle|R$144,88|28394|752|640|245|38,28%|R$0,59|
|3|2026-11-07–2026-11-09|Experimental|R$464,29|74333|2401|2001|699|34,93%|R$0,66|
|3|2026-11-07–2026-11-09|Controle|R$470,34|93177|2280|1924|724|37,63%|R$0,65|
|7|2026-11-03–2026-11-09|Experimental|R$1026,22|175275|5471|4550|1584|34,81%|R$0,65|
|7|2026-11-03–2026-11-09|Controle|R$1029,58|235793|5395|4509|1662|36,86%|R$0,62|
|14|2026-10-27–2026-11-09|Experimental|R$2093,48|361894|10439|8781|3184|36,26%|R$0,66|
|14|2026-10-27–2026-11-09|Controle|R$2107,05|501520|11343|9546|3604|37,75%|R$0,58|

**Novidades/incerteza:** experimental36,77→35,49%(−1,28p.p.),controle36,18→38,28% em08→09/nov. Diferença diária−2,79p.p.,IC95%nominal−8,09a+2,50;7d−2,05p.p.,IC95%−4,02a−0,07;14d−1,49p.p.,IC95%−2,89a−0,10. Exclusão nominal dezero nasjanelas móveis não estabelece causalidade depois demúltiplasleituras/eventosatribuídos/dependentes/campanhasdistintas. Semanas27/out–02/nov→03–09/nov:experimental37,82→34,81%(−3,00p.p./−7,94%relativo),controle38,55→36,86%(−1,70p.p./−4,40%);diferençaentre mudanças−1,31p.p.,IC95%−4,11a+1,49,entre evoluçõesrelativas−3,54pontospercentuais. Não são resultados doCRO-002não publicado. Revisão08/novcontroleR$174,09→174,10/impressões35817→35819;LPV/Leadsiguais,snapshotspreservados.

**Entrega analítica nova:** campanha120252642171330505 criada09/nov21:35:31SP,orçamentoR$50;campanha/conjunto120252642175430505/anúncio120252642196110505todosPAUSED. MCPgasto/impressões0,cliques/LPV/Leadnull;Graph09–10/novdata[],sem linhasretornadas,não converter null emzero. Criativo usa postcujo GETfalhoucode10;destino efetivo não confirmado pelo nome/UTM. Não incluirclone nos totais ou culparpelo gap. Atividades35registros08–10/nov/paginaçãoesgotada,IDsnovosincluídos. ContinuaçãoMCP mostrou4rascunhos versus3:novopara anúnciooriginalativo120251541120490505,atualizado09/nov21:58:47SP,media_sourcing_spec.bodies2→7eobject_story_id→null;asset_feed_spec.bodiescontinua2. Livecriativo2214895639068786/copy/URL/UTM/efetivopostinalterados,semprova depublicação. Guardliteraldeobject_story_idfalhoupoisGraphomitecampo;effective_object_story_idpermaneceigual,diagnósticopreservado,ausêncianãoprova aplicação. **Gestoribombonato:confrontarpendêncianovadoanúnciooriginalcomliveantesdepublicaçãomanualemlote;confirmardestinodo clonecasodecidafuturamenteativá-lo.** Nenhumapublicação/ativação/ediçãoMetapeloagente. BL-02ICE8/5/8refinado:conferirnovascampanhas e drafts dosadsjáativos,registrarprimeiraentrega/ediçãoefetiva,nãomera descoberta comoexposição. Primáriaagregada/pesospré-fixados/coberturasensibilidadeseparadospreservados;semnovo gatearbitrário ouID. Pedidosmateriais23/out/comprovação20.000/estrelas03/novpendentes,semnovacobrança.

**Contexto/publicação/QA:**12diascompletosdesde29/out,8025LPV/2912Leads=36,29%;09/novnãorepetequasezero28/out,causaaindadesconhecida. Ambas campanhasalvoACTIVE/R$150,quatroadsativosnaexperimental/umcontrole,conjuntoseconfiguraçãoliveinalterados;diferençabrutasomente miniaturaassinada doantigoPAUSED. Novosadsde21/outsomam516LPV/171Leads=81,39%dosLPV;decomposição08→09/nov−1,28p.p.=+0,08composição−1,36dentro,aritméticanãocausal. Android154/412=37,38%,iPhone71/222=31,98%,semdiagnósticoSafari. Pagesdeployment7674620136success10/nov05:44:49Z/Actions42763950380successparaSHAab142e82527029473ff3adadaca8ddc98b78273a;ambosHTMLsHTTP200/byteabyteiguaisàmain. Mudanças humanasapenasconvites nasduaslandings,verificadaspordiff,nãoresetamavaliação. Verdeantigopublicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto. CandidatolocalversusmainapenasduascoresCSS,controle/scripts/copy/convitespreservados;NodeVMprodução/proposta10casos+igualdadehref/constantePASSemcada,semrede/Leadreal/join. SemnovoHTML/CSS,novaQAvisualnão repetida. GateCRO-002:restaurarGitHub/sincronizar#16,decisãohumana,depoisPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste.

**Operação/próximo:**09/novexecuçãoec4e7bd220c0486b94750e851f1ff6b8completed12:08:40Z;ponteTelegramrecibo19990às12:10:39Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat/próximaexecução11/nov12hUTCconfirmados,semalteraçãoagenda/serviço/credencial/outroperfil. Próximaobservação11/nov09hSPinclui10/novcompleto:gapCVRsemanal,mix/rascunho/cloneefetivamenteveiculadoouaindapausado,autenticação/sincronização/decisão#16,eventualretornodecomprovaçãoerecibo. Histórico/notapreservadoslocalmenteem`~/work/hermes-scratch/cro-icb-2026-11-10/`;PRnãoatualizado,semmerge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-11

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out reconsultado sem revisão e sem reabrir. [BL-02 — sensibilidade de dia da semana e proteção contra falso lift](cro/research/2026-11-11-weekday-sensitivity-and-false-lift-guard.md): série por anúncio/dia03–10/nov conciliada e plano futuro refinado com cobertura de TODOS os dias comuns, sem escolher só uma terça favorável. Nenhum tratamento novo. **Histórico01–11/nov LOCAL:** GETGitHub/userHTTP401Badcredentials persiste; nenhuma escrita remota tentada. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, sincronizar#16commain/histórico antes de decisão humana; branchremota ainda contém16.000/convite anterior.

**Fontes:** início09hSãoPaulo, snapshot2026-11-11T12:02:35.685391+00:00. Origin/main/históricos integrais main/PRs pendentes/diário local, PRs abertos/fechados/commits consultados. Worktree isolada incorpora mainab142e8 e commitlocal6e9bf7e preservando todos registros. MCPoficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados;1/3/7/14dias conciliados exatamente com GraphGET diário29/set–10/nov emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, paginação/continuações verificadas. Ad/device/placement eentrega diária/horária conciliados; resíduo monetário de posicionamento controleR$0,000001, contagens/totaisprincipaisexatos.11/novparcial excluído. **Lead=proxy pré-navegação, não participante confirmado; baselinehistórico36%semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-10–2026-11-10|Experimental|R$143,65|19988|681|569|203|35,68%|R$0,71|
|1|2026-11-10–2026-11-10|Controle|R$137,77|24813|662|562|185|32,92%|R$0,74|
|3|2026-11-08–2026-11-10|Experimental|R$461,32|72085|2336|1959|706|36,04%|R$0,65|
|3|2026-11-08–2026-11-10|Controle|R$456,75|89026|2244|1904|684|35,92%|R$0,67|
|7|2026-11-04–2026-11-10|Experimental|R$1012,56|160545|5115|4271|1519|35,57%|R$0,67|
|7|2026-11-04–2026-11-10|Controle|R$1020,20|210669|5081|4276|1571|36,74%|R$0,65|
|14|2026-10-28–2026-11-10|Experimental|R$2064,75|341842|10247|8610|3119|36,23%|R$0,66|
|14|2026-10-28–2026-11-10|Controle|R$2084,42|486554|11108|9325|3484|37,36%|R$0,60|

**Novidades/incerteza:**10/novexperimental35,49→35,68%(+0,19p.p.),controle38,28→32,92%(−5,36p.p.). A vantagem diária+2,76p.p.,IC95%nominal−2,77a+8,29, veio sobretudo da queda do controle, não de grande recuperação experimental.7d−1,17p.p.,IC95%−3,21a+0,86;14d−1,14p.p.,IC95%−2,55a+0,28. Semanas28/out–03/nov→04–10/nov:experimental36,87→35,57%(−1,31p.p./−3,55%relativo),controle37,89→36,74%(−1,15p.p./−3,03%);diferença entre mudanças−0,16p.p.,IC95%−2,99a+2,67,entre evoluçõesrelativas−0,52pontospercentuais. Ontem osICs móveis excluíamzero e hoje não: leituras sequenciais/campanhasdistintas/eventosatribuídos/dependentes impedem vitória causal ou seleção oportunista. Nenhuma taxa medeCRO-002não publicado. Revisão09/novexperimentalR$142,87→142,88/impressões22509→22511;LPV/Leadsinalterados,snapshots preservados.

**Aprendizado/ação preparada:** terças03→10/novexp.268/848=31,60%→203/569=35,68%,controle276/795=34,72%→185/562=32,92%;diferençaentremudanças+5,87p.p.,IC95%−1,29a+13,04,apenasdiagnóstico. Mudançaexperimental+4,07p.p.=−1,70composição+5,77dentro dosanúncios;taxapadronizadapelos pesos03/nov36,11%,célulaspequenas explicitadas. PlanoBL-02mantémprimáriacumulativa/ICE8/5/8/compactaçãoúnica eacrescenta sensibilidade de calendário sobre todosdiascomuns,sem substituir endpoint pelo par favorável ou alterar plano4170doCRO-002. NenhumIDnovo. Pedidos23/out/comprovação20.000/estrelas03/novpendentes,semnovacobrança.

**Exposição/contexto/QA:** ambas campanhasalvoACTIVE/R$150,quatroadsativos naexperimental/umcontrole; ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoiguaisàvéspera. Diferençabruta sóminiaturaassinada doantigoPAUSED. Clone120252642171330505/hierarquiaPAUSED;Graph09–10/novdata[],destinoefetivo permanece não confirmado; nãoincluí-lo nostotais. MCPhoje não ofereceu next_actions,mas consultadraft explícita namesmasessão/conversa confirmou4rascunhos com mesmosIDs/time_updated/status/valoresnovos;diferençadepayload somente omissão deoldcontextual,sem prova depublicação/remoção.86atividadesGraphdesde21/out/paginaçãoesgotada,semnovaediçãorelevantealvo.13diascompletosdesde29/out8594LPV/3115Leads=36,25%;10/novnão repetiu quasezero28/out,causaaindadesconhecida. Novosads21/out489LPV/172Leads=85,94%dosLPV;Android138/373=37,00%,iPhone65/195=33,33%,semdiagnósticoSafari.

**Publicação/gates:** mainab142e82527029473ff3adadaca8ddc98b78273a inalterada;deployment7674620136success/Actions42763950380success eHTMLpúblicoHTTP200deambaslandingsbyteabyteiguaisàmain;verdeantigopublicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews;#31operacionalaberto. Guardlocal:candidatoversusmainapenasduascoresCSS,controle/scripts/copy/convitespreservados;NodeVMprodução/proposta10casos+igualdadehref/constantePASSemcada,semrede/Leadreal/join. SemnovoHTML/CSS,novaQAvisualnão repetida. GateCRO-002:restaurarGitHub/sincronizar#16,decisãohumana,depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste.

**Operação/próximo:**10/novexecução7dacc9e8d89744b68d8fd210bea50a99completed;ponteTelegramrecibo20080às2026-11-10T12:15:39.760252+00:00,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat epróximaexecução12/nov12hUTCconfirmados;nenhumaagenda/serviço/credencial/outroperfilalterado. Próximaobservação12/nov09hSPinclui11/novcompleto:CVRdo controle apósqueda,mix/rascunhos/clone,autenticação/sincronização/decisão#16,eventualretornodecomprovaçãoerecibo. Histórico/notapreservadoslocalmenteem`~/work/hermes-scratch/cro-icb-2026-11-11/`;PRnãoatualizado,semmerge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-12

**Estado vigente/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out reconsultado sem revisão e sem reabrir. [BL-02 — diagnóstico da cadeia CPL e proteção da próxima avaliação](cro/research/2026-11-12-cpl-funnel-chain-and-next-test-guard.md): decomposição verificável de duas semanas completas, anúncios/dispositivos/posicionamentos conciliados e plano futuro refinado para não confundir CPM/CPL com resposta da landing. Nenhum tratamento novo. **Histórico01–12/nov LOCAL:** GitHubGET/userHTTP401Badcredentials persiste; gh também sem login. Nenhuma escrita remota tentada. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, sincronizar#16commain/histórico e então decidir; branchremota ainda contém16.000/convite anterior.

**Fontes:** início09hSãoPaulo; métricas principais consolidadas2026-11-12T12:02:51Z. Origin/main e históricos integrais main/PRs pendentes/diário local lidos; PRs abertos/fechados/commits conferidos. Worktree isolada preserva2af5b8a/todos registros. MCPoficial read-only inicializado, protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados; quatro janelas conciliadas exatamente comGraphGET diário29/set–11/nov emgasto/impressões/cliques/LPV/Leads, aliases selecionados, atribuição unificada preservada, paginação/continuações verificadas. Ad/device/placement eentrega diária/horária conciliados; resíduosmonetários do último dia−R$0,000001 nosdoisbreakdownscontrole, contagens/totaisprincipaisexatos. AtividadesGraphHTTP500code2transitório recuperado emretry, semusar snapshotsantigos/relaxarguard.12/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado; baselinehistórico36%semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-11–2026-11-11|Experimental|R$146,93|21114|659|522|175|33,52%|R$0,84|
|1|2026-11-11–2026-11-11|Controle|R$146,70|24933|605|517|184|35,59%|R$0,80|
|3|2026-11-09–2026-11-11|Experimental|R$433,47|63615|2092|1725|603|34,96%|R$0,72|
|3|2026-11-09–2026-11-11|Controle|R$429,37|78142|2019|1719|614|35,72%|R$0,70|
|7|2026-11-05–2026-11-11|Experimental|R$1057,97|164952|5217|4332|1510|34,86%|R$0,70|
|7|2026-11-05–2026-11-11|Controle|R$1055,43|208550|5057|4257|1564|36,74%|R$0,67|
|14|2026-10-29–2026-11-11|Experimental|R$2208,89|362367|10890|9116|3290|36,09%|R$0,67|
|14|2026-10-29–2026-11-11|Controle|R$2077,29|474819|10858|9110|3372|37,01%|R$0,62|

**Novidades/incerteza:** experimental35,68→33,52%(−2,15p.p.),controle32,92→35,59%(+2,67p.p.) em10→11/nov; diferença diária−2,07p.p.,IC95%nominal−7,85a+3,72;7d−1,88p.p.,IC95%−3,91a+0,14;14d−0,92p.p.,IC95%−2,32a+0,47. Semanas29/out–04/nov→05–11/nov:experimental37,21→34,86%(−2,35p.p./−6,32%relativo),controle37,26→36,74%(−0,52p.p./−1,38%);diferença entre mudanças−1,83p.p.,IC95%−4,63a+0,96,entre evoluçõesrelativas−4,93pontospercentuais. Experimental7d−1,14p.p.versus36,semtestecontra baseline semdenominador. Eventosatribuídos/dependentes,campanhasdistintas,mix eediçãovisívelexterna02/nov limitamcausalidade;nenhuma taxa éresultado doCRO-002não publicado. Revisões10/nov:exp.R$143,65→143,66/impressões19988→19990;controleR$137,77→137,79/impressões24813→24815;LPV/Leadsinalterados,snapshotspreservados.

**Entrega analítica:** CPLexperimental semanal+8,36% econtrole+19,40% têm componentes diferentes. NaexperimentalCPM+10,01% eCTRlink+10,06% quase secompensam;LPV/clique84,33→83,04% eCVR37,21→34,86% pressionam oCPL. No controleCPM+31,87%,CTR+11,30%,CVRquaseestável37,26→36,74%. IdentidadeCPL=CPM/(1000×CTR×LPV/clique×CVR) edec.logarítmica aprovadas semarredondar. Decomposição marginalporanúncio daquedaexperimental−2,35p.p.=−0,97composição−1,38dentro,aritméticanãocausal. Androidexperimental39,97→36,53%,iPhone31,96→31,91%;não apontaSafari como causa. PlanoBL-02ICE8/5/8/compactaçãoúnica preservado, acrescentando cadeiaCPLcomo diagnóstico secundário, nunca substituição daprimáriaCVR/endpoint conforme custodeleilão. Não muda plano4170doCRO-002,não cria outro gate ouID. Pedidosmateriais23/out/comprovação20.000/estrelas03/novpendentes,semnovacobrança.

**Exposição/QA/gates:** campanhasalvoACTIVE/R$150,quatroadsativosnaexperimental/umcontrole; ativos/conjuntos/copy/destinos/UTMs/tracking/atribuiçãoigualàvéspera, diferença brutaapenasminiaturaassinada doantigoPAUSED. Clone120252642171330505 efilhosPAUSED,Graph09–11/novsem linhas/destinoefetivonão confirmado. Draft explícito namesmasessão/conversa confirma4rascunhos com mesmosIDs/conteúdos/time_updated,semadição/remoção/diferença devalores;semprova denovapublicação.87atividadesGraphdesde21/out/paginaçãoesgotada,semnovaediçãorelevantealvo.14diasdesde29/out9116LPV/3290Leads;11/novnão repetiuquasezero28/out,causaoriginalaindadesconhecida. Novosads21/out468LPV/156Leads=89,66%dosLPVdiários.

Mainab142e82527029473ff3adadaca8ddc98b78273a inalterada;deployment7674620136success/Actions42763950380success eHTMLpúblicoHTTP200deambaslandingsbyteabyteiguaisàmain;verdeantigopublicado. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews. Novos#38/#39 são somenteconvitesexperimental/controle; ambospropõemmesmoinvite,maspendentes,nãoincorporados;#40fora daslandingsmedidas e#31anteriorcontinuaaberto. CandidatolocalversusmainapenasduascoresCSS;controle/scripts/copy/convitespreservados. NodeVMprodução/proposta10casos+igualdadehref/constantePASSemcada,semrede/Leadreal/join. NenhumHTML/CSSnovo,novaQAvisualnão repetida. **Gate:**restaurarGitHub/sincronizar#16antesde decisãohumana,depoisconfirmarPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste.

**Operação/próximo:**11/novexecução109e7c265b5a49ac83501d6b067cab7ccompleted;ponteTelegramrecibo20188às2026-11-11T12:10:38.935754Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat epróximaexecução13/nov12hUTCconfirmados;nenhumaagenda/serviço/credencial/outroperfilalterado. Próximaobservação13/nov09hSPinclui12/novcompleto:CVR/CPL ecomponentes,mix/drafts/clone,autenticação/sincronização/decisão#16,eventuaisrotaçõeshumanas/retornodecomprovaçãoerecibo. Histórico/notapreservadoslocalmenteem`~/work/hermes-scratch/cro-icb-2026-11-12/`;PRnãoatualizado,semmerge/auto-merge/deployoualteraçãoMeta/controle/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-13

**Estado/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 continua **Inconclusivo**, endpoint14–21/out reconsultado sem revisão e sem reabrir. [Auditoria de integração e handoff](cro/research/2026-11-13-three-way-merge-safety-and-blocker-handoff.md): simulação local de três vias demonstrou que a integração exata da main atual com o head do #16 preserva convites/conteúdo humano atuais, alterando somente as duas cores na experimental. **Correção das notas anteriores:** snapshot antigo da branch não prova que merge reverteria main; nenhuma regressão foi demonstrada nessa simulação. Gate de autenticação/diário pendente e decisão humana permanece, não um conflito presumido. GitHubGET/userHTTP401Badcredentials persiste; nenhuma escrita remota tentada. Histórico de novembro permanece LOCAL, sem alegar atualização doPR.

**Fontes:** execução09hSãoPaulo; snapshot2026-11-13T12:02:43Z. Origin/main atualizado; história integralmain/PRs pendentes/diário local lida, versões remotas adicionais comprovadas como main ou prefixo exato do histórico local lido; PRs abertos/fechados/commits conferidos. Worktree isolada da mainc0f29ef, preservando registros anteriores. MCPoficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados; quatro janelas conciliadas exatamente comGraphGET diário29/set–12/nov emgasto/impressões/cliques/LPV/Leads; aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente. Ad/device/placement eentrega diária/horária conciliados, resíduosmonetários do último diazero.13/novparcial excluído. **Lead=proxy pré-redirecionamento, não entrada confirmada; baseline histórico36%semdenominador apenas descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-12–2026-11-12|Experimental|R$143,57|20252|683|552|174|31,52%|R$0,83|
|1|2026-11-12–2026-11-12|Controle|R$147,31|23155|628|528|198|37,50%|R$0,74|
|3|2026-11-10–2026-11-12|Experimental|R$434,17|61357|2023|1643|552|33,60%|R$0,79|
|3|2026-11-10–2026-11-12|Controle|R$431,80|72904|1895|1607|567|35,28%|R$0,76|
|7|2026-11-06–2026-11-12|Experimental|R$1028,69|156613|5021|4153|1416|34,10%|R$0,73|
|7|2026-11-06–2026-11-12|Controle|R$1036,42|193692|4840|4082|1501|36,77%|R$0,69|
|14|2026-10-30–2026-11-12|Experimental|R$2180,46|345289|10737|8957|3188|35,59%|R$0,68|
|14|2026-10-30–2026-11-12|Controle|R$2084,60|464885|10722|8976|3328|37,08%|R$0,63|

**Novidades/incerteza:** experimental33,52→31,52%(−2,00p.p.),controle35,59→37,50%(+1,91p.p.). Diferença diária−5,98p.p.,IC95%nominal−11,64a−0,31;7d−2,68p.p.,IC95%−4,74a−0,61;14d−1,48p.p.,IC95%−2,89a−0,08. Wilson7dexperimental32,67–35,55/controle35,31–38,26. Semanas30/out–05/nov→06–12/nov:experimental36,89→34,10%(−2,79p.p./−7,56%relativo),controle37,33→36,77%(−0,56p.p./−1,50%);diferença entre mudanças−2,23p.p.,IC95%−5,05a+0,59,entre evoluçõesrelativas−6,06pontospercentuais. Experimental7d−1,90p.p.versus36,semtestecontra baseline semdenominador. Exclusão nominal de zero em janelas móveis não estabelece causalidade após múltiplasleituras/campanhasdistintas/eventosatribuídos/dependentes/mix. Nenhuma taxa medeCRO-002aindanão publicado. Revisão11/novexperimentalR$146,93→146,94/impressões21114→21115;controle24933→24934impressões;LPV/Leadsiguais,snapshots preservados.

**Exposição:** ambas campanhasalvoACTIVE/R$150,quatroadsativosnaexperimental/umcontrole; uniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição inalterados, diferença bruta apenasminiaturaassinada doantigoPAUSED. Draft explícito mesma sessão/conversa: quatro rascunhos byte-equivalentes emdados aos consultadosontem, sempublicaçãoinferida. Clone120252642171330505/filhosPAUSED,Graph09–12/novsem linhas,destinoefetivonão confirmado; fora dos totais. Novosads21/out516LPV/163Leads=93,48%dosLPVdiários; nãoatribuir oscilação àcor não publicada. Incidente28/outpreservado/causaoriginaldesconhecida;12/novnão repete quasezero.

**Publicação/QA/encaminhamento:** humanos mesclaram#38/#39 e rotacionaramcontroleporcommitdireto; diff desdeab142e8 contém somentehref/constanteemcada landing. Main`c0f29ef85bf45eb4380cdd409456b1af9c976e17`,deployment7749322998success12/nov20:51:15Z/Actions43304285233success,ambosHTMLsHTTP200/byteabyteiguaisàmain;coresantigaspublicadas. Novo#42operacionalsóURLs experimentalpendente;#31continuaaberto,semdecisãodoagente. Simulação`merge-tree`exit0/árvore3b8f76b150eca05e80074f314123426fe15fec39 não moveu refs nempublicou:resultadoindex3exatamentemain+duascoresCSS,controleidêntico;copiaralegaçãonãovalida20.000. Fonteproduction/candidatooffline:guardescopoPASS,NodeVMigualdadehref/constante+10casosPASSemcada,semrede/Leadreal/join. Falha inicialdohelperpreservada:esperavacontrastenoHTMLdarepo numaexecuçãodocs-only;corrigidoparavalidarcandidatoexclusivamentescratch,semalterarlandingourelaxarescopo. NenhumanovaQAvisualporquenãohouveimplementaçãonova;capturasPRcontinuamoriginais,nãoSafari/WebVitals.

**Gate/ação/responsável:** ibombonato/@hermes restaurarautenticaçãosegura/identidade/permissão e incorporar diário local ao mesmoPR; decidir manutenção#42/#31e#16semmergeautomático. Revalidar simulaçãoquando main/headmudarem; snapshotantigonãoéprova dereversão. SóapóspublicaçãoPagesSHA+HTMLcongelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste. BL-02ICE8/5/8/fallbacksemmaterial refina checklist para resultado real daintegração,semnovotratamento/ID/gateestatístico. Pedidosmateriais23/out/comprovação20.000/estrelas03/novpendentes,semcobrançarepetida.

**Operação/próximo:**12/novexecução07541da2ad894e229d5478588ea94143completed12:08:57Z;ponteTelegramrecibo20270às12:10:38Z,ID/handle/hashSHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual;entregadesterelatóriosóapósconclusão,semenviopróprio. Schedulerhostativo/heartbeat/próximaexecução14/nov12hUTC,semalteraçãoagenda/credencial/serviço/outroperfil. Próximaleitura14/nov09hSPinclui13/novcompleto:CVRsemanal/mix,autenticação/diário/decisão#16,main/headapóspossíveisrotaçõese recibo. Artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-11-13/`,histórico/notaemcommit/patchlocal;semPRatualizado/merge/auto-merge/deployoualteraçãoMeta/controle/HTML/rastreamento/destinopeloagente.

## Acompanhamento diário — 2026-11-14

**Estado/decisão:** CRO-002 **Em PR #16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out reconsultado sem revisão e sem reabrir. **Entrega concreta:** [BL-02 — separar perda clique→LPV da resposta ao CTA](cro/research/2026-11-14-lpv-link-efficiency-and-next-test-guard.md), com duas semanas completas por anúncio/dispositivo conciliadas e novo guard de denominadores/cobertura no plano futuro. Nenhum tratamento novo. **Histórico de novembro continua LOCAL:** GitHub GET/user401Badcredentials e gh sem login; nenhuma escrita remota tentada, causa da falha não presumida. ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão e sincronizar diário preservado; decisão humana sobre #16 é gate separado.

**Fontes:** início09hSãoPaulo; snapshot principal2026-11-14T12:02:15Z. Origin/main atualizado; históricos integrais main/PRs pendentes/diário local lidos, versões remotas confirmadas como main ou prefixo exato do histórico lido, PRs abertos/fechados/commits consultados. Worktree isolada da main atual, todos registros preservados. MCP oficial read-only inicializado/protocolo2025-11-25 negociado/reutilizado, schemas/campos/conta consultável confirmados; quatro janelas conciliadas exatamente com Graph GET diário29/set–13/nov emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, sem paginação/continuação pendente. Anúncios/device/placement e entrega diária/horária conciliados, resíduos monetários do último diazero. 14/novparcial excluído. **Lead=proxy de clique antes de navegar, não participante confirmado; baseline histórico36% semdenominador é descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-13–2026-11-13|Experimental|R$139,21|19030|654|510|194|38,04%|R$0,72|
|1|2026-11-13–2026-11-13|Controle|R$144,09|23351|578|478|182|38,08%|R$0,79|
|3|2026-11-11–2026-11-13|Experimental|R$429,72|60397|1996|1584|543|34,28%|R$0,79|
|3|2026-11-11–2026-11-13|Controle|R$438,10|71440|1811|1523|564|37,03%|R$0,78|
|7|2026-11-07–2026-11-13|Experimental|R$1037,68|154722|5078|4154|1445|34,79%|R$0,72|
|7|2026-11-07–2026-11-13|Controle|R$1046,23|189432|4753|4009|1473|36,74%|R$0,71|
|14|2026-10-31–2026-11-13|Experimental|R$2151,37|336115|10622|8829|3157|35,76%|R$0,68|
|14|2026-10-31–2026-11-13|Controle|R$2086,34|456241|10491|8786|3258|37,08%|R$0,64|

**Desde ontem/incerteza:** experimental31,52→38,04%(+6,52p.p.),controle37,50→38,08%(+0,58p.p.). Recuperação diária não demonstra ganho sustentável: diferença13/nov−0,04p.p.,IC95%nominal−6,09a+6,02;7d−1,96p.p.,IC95%−4,04a+0,12;14d−1,32p.p.,IC95%−2,75a+0,10. Wilson7dexperimental33,35–36,25/controle35,26–38,25. Semanas31/out–06/nov→07–13/nov:experimental36,62→34,79%(−1,83p.p./−5,01%relativo),controle37,37→36,74%(−0,62p.p./−1,67%);diferença entre mudanças−1,21p.p.,IC95%−4,06a+1,64,entre evoluções relativas−3,34pontospercentuais. Experimental7d−1,21p.p.versus36,semtestecontra baseline semdenominador. Campanhas distintas/eventos atribuídos/dependentes/leituras sequenciais/mix limitam causalidade; nenhuma taxa medeCRO-002não publicado. Nenhuma revisão dos dias comuns em relação ao snapshot13/nov, registros preservados.

**Aprendizado novo:** LPV/clique experimental84,33→81,80% nas semanas completas, controle83,25→84,35%. Decomposição por anúncios, cobrindo todoscliques/LPV:−2,52p.p.=−0,80composição−1,72dentro dosanúncios. Não é prova de velocidade/caso individual. Androidsmartphone experimental80,15→76,38%,iPhone93,71→94,76%;não diagnosticarSafari/Android. Dispositivos comuns não cobrem integralmente a campanha: denominadores/células excluídas explícitos na nota e raws, sem imputação. Não somar decomposições marginais. BL-02ICE8/5/8/compactaçãoúnica preservado;novo guard separa LPV/clique de Lead/LPV e congela pesos do denominador próprio. Não prometer performance pela geometria nem tornar investigação adicional gate arbitrário do contraste. PrimáriaCVR/endpoint e plano4170CRO-002 inalterados. Pedidos23/out/comprovação20.000/estrelas03/nov pendentes, sem cobrança repetida.

**Exposição/publicação/QA:** ambas campanhasalvoACTIVE/R$150,quatroadsativosnaexperimental/umcontrole; uniãoIDs/ativos/conjuntos/copy/destinos/UTMs/tracking/atribuição inalterados; diferença bruta apenasminiaturaassinada doantigoPAUSED. Quatro drafts explícitos na mesma sessão/conversa idênticos aos deontem; clone120252642171330505/filhosPAUSED,Graph09–13/novsem linhas, destinoefetivonão confirmado; fora dostotais. 90atividadesGraph/paginaçãoesgotada,semnovaedição relevante alvo. Anúncios de21/out449LPV/175Leads=88,04%dosLPV13/nov. Incidente28/outpreservado/causaoriginaldesconhecida;13/novnão repetequasezero.

Humanos integraram#42experimental/#44controle, somentehref/constante;#43fora daslandingsmedidas. Pagesdeployment7781105426success14/nov02:14:24Z/Actions43545103765success paraSHA`e58525718798b40031e2cb18974f50ccb64cfdf1`;ambosHTMLsHTTP200/byteabyteiguaisàmain,coresantigaspublicadas. Novo#45operacionalexperimentalaberto,sóURLs,nãoincorporado;#31anterioraberto. #16aberto/headf9286a3/semmerge/auto-merge/semcomentários/reviews. Simulação main+#16 árvore45de49b184060559ed2804c2f90cde9a617d43cf/exit0: index3exatamentemain+duascores,controleidêntico;nenhumarefmovida/merge/publicação. Revalidarse main/headmudar,nãoafirmarreversãopelo snapshotantigo. Guardlocal/NodeVMprodução/proposta:igualdadehref/constante+10casoscomportamentaisPASSemcada,semrede/Leadreal/join. Nenhuma implementaçãoHTML/CSS,novaQAvisualmobile não repetida;capturasPRoriginais,nãoSafari/WebVitals. Falhas locais iniciais doshelpers (candidatoaindanãogerado e end/__file__ ausentes) corrigidas,saídasfalhaspreservadas;gates finais passaram semrelaxarescopo oufabricardados.

**Gate/próximo passo:** ibombonato/@hermes restaurarGitHub/sincronizarhistórico;ibombonatodecidir#16. DepoisdepublicaçãoconfirmadaPagesSHA+HTML,congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NãofaltamLPVdoCRO-001oumaterialparacontraste. Diário/nota mantidoslocalmente,PRnãoatualizado. Próximaleitura15/nov09hSPinclui14/novcompleto:CVRsemanal/LPVclique/mix,autenticação/decisão#16/eventualrotação#45 e recibo deste ciclo.

**Operação:** execução13/nov991cdc3c40e743d6a7bb14f3f7f1ad5ccompleted;ponteTelegramrecibo20337às12:10:40Z,ID/handle/SHA256daresposta finalextraídaconferidos. Falha23/outnãoéestadoatual;entregadehojesóapósconclusão,semenviopróprio. Nenhumaagenda/serviço/credencial/outroperfilalterado. Artefatosatuaisem`~/work/hermes-scratch/cro-icb-2026-11-14/`,histórico/nota/patchlocal;semPRnovo/merge/auto-merge/deployoualteraçãoMeta/controle/HTML/rastreamento/destinopeloagente.


## Acompanhamento diário — 2026-11-15

**Decisão/entrega concreta:** CRO-002 **Em PR #16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão e não reaberto. Autenticação GitHub voltou a responder HTTP200 no GET/user como ibombonato; permissão push confirmada no repositório. Causa da restauração não presumida; nenhuma credencial alterada pelo agente. Sincronizar nesta execução o MESMO PR#16 com todo o diário/pesquisas01–14/nov, main atual, convites humanos e alegação20.000 não validada, mantendo exclusivamente duas coresCSS como tratamento. Capturas atuais390×844/360×800 renderizadas/reinspecionadas. Sem segundo experimento/ID, merge remoto/auto-merge/deploy. O readback remoto final é condição para declarar sincronização, registrado em remote-sync-verification.json.

**Fontes:** início09hSãoPaulo; snapshot principal 2026-11-15T12:02:40.571724+00:00. Históricos integrais main/PRs pendentes/diário local lidos, PRs abertos/fechados/commits consultados. MCP oficial somente leitura inicializado/protocolo negociado reutilizado, schemas/conta consultável/campos confirmados; janelas1/3/7/14dias conciliadas exatamente com GraphGET diário29/set–14/nov emgasto/impressões/cliques/LPV/Leads. Aliases selecionados, atribuição unificada preservada, paginação/continuações verificadas. Anúncios/device/placement eentrega diária/horária conciliados; resíduos monetários permitidos abaixo de1centavo documentados em today-validation.json, sem relaxar contagens/totaisprincipais.15/nov parcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado. Baseline histórico36% semdenominador: referência descritiva.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-14–2026-11-14|Experimental|R$158,82|21593|727|608|221|36,35%|R$0,72|
|1|2026-11-14–2026-11-14|Controle|R$154,94|24024|621|526|182|34,60%|R$0,85|
|3|2026-11-12–2026-11-14|Experimental|R$441,62|60877|2064|1670|589|35,27%|R$0,75|
|3|2026-11-12–2026-11-14|Controle|R$446,34|70530|1827|1532|562|36,68%|R$0,79|
|7|2026-11-08–2026-11-14|Experimental|R$1049,89|154079|5059|4151|1470|35,41%|R$0,71|
|7|2026-11-08–2026-11-14|Controle|R$1049,81|184492|4676|3953|1430|36,18%|R$0,73|
|14|2026-11-01–2026-11-14|Experimental|R$2099,83|329819|10470|8671|3076|35,47%|R$0,68|
|14|2026-11-01–2026-11-14|Controle|R$2099,78|448435|10345|8668|3184|36,73%|R$0,66|

**Novidade externa relevante — não confundir com CRO:** controle alterou targeting em14/nov15:48:40SP, confirmado por Graphactivities e readback: device_platforms mobile+desktop→mobile; geo_locations.location_types home+recent→frequently_in+home+recent. Reentrada de revisão/status do anúncio até15:51:43SP; creative/copy/destino/UTM/atribuição consultados permanecem iguais. Ambos orçamentos-alvoR$150/dia, experimental inalterada.14/nov é dia de transição do controle; primeiro dia completo dessa configuração15/nov, disponível16/nov. Não inferir mudança real do mix por uma configuração, causa da CVR ou autorização para editar Meta. Preservar série principal; na futura avaliação do contraste registrar fases e sensibilidades, sem selecionar baseline mais favorável ou impor espera arbitrária.

**Outro funil ativo na mesma landing:** clone120252642171330505 antesPAUSED agoraACTIVE/R$50dia, conjuntoACTIVE, dois anúnciosACTIVE e umPAUSED. Ativação campanha14/nov15:33:51SP; primeira entrega do anúncio120252642196110505às15:39:13SP e120252736506790505às20:12:01SP. Desta vez object_story_spec.link_data.link de ambos ativos confirma index3.html; post efetivoGET ainda retorna code10/permissão, não foi visto. Métricas14/nov do clone, SEPARADAS das duas campanhas-alvo: R$83,06/14777impressões/302cliques/251LPV/84Leads/CVR33,47%/CPLR$0,99. MCP/Graphdiário+horário e ad-day conciliados; ad principal247LPV/82Leads e segundo4/2. Snapshot inicial Graph14776impressões versus atual14777 preservado em clone-current.json/external-exposure-initial.json; releitura atual conciliou exatamente. Atividades de outros IDs de primeira entrega também preservadas, não inventar configuração desses IDs. **Não somar clone à campanha experimental nem chamar seus Leads de participantes únicos; registrar como exposição adicional ao mesmoHTML/Pixel**, sem concluir canibalização/impacto. Handoff ao gestoribombonato: considerar esse lançamento e a edição do controle na leitura dos próximos dias; nenhumapublicação/ativação/alteraçãoMeta pelo agente.

**Diagnóstico/incer­teza:** CVR14/nov 36,35% versus 34,60%; diferença+1,75p.p.,IC95%nominal -3,83a+7,33.7d diferença -0,76p.p.,IC95% -2,85a+1,33; não demonstra superioridade. Semanas01–07→08–14/nov:experimental35,53→35,41%(−0,12p.p./−0,33%relativo),controle37,20→36,18%(−1,03p.p./−2,76%); diferença entre evoluçõesrelativas+2,42pontospercentuais, descritiva. Eventosatribuídos/dependentes,campanhasdistintas,múltiplasleituras,mix e mudanças externas limitamcausalidade; nenhuma taxa medeCRO-002não publicado. Revisão13/nov experimentalR$139,21→139,23/impressões19030→19032;LPV/Leadsiguais, snapshotsanteriores preservados. Quatro drafts explícitos iguais àvéspera; não inferir publicação pelo clone ativado. Experimental mantém quatroativos/umPAUSED e novosads21/out538LPV/192Leads=88,49%dosLPVdiários. Incidente28/outpreservado/causaoriginaldesconhecida,14/novnão repetequasezero.

**Publicação/QA:** humanos integraram#45/#46, diff desdee585257 apenas href/constante emindex3, controle intacto. Pagesdeployment7795783732success14/nov23:56:47Z/Actions43655676470success paraSHAa98cb8358e14186654b68ed01e7b634a94c77e8e;ambosHTMLsHTTP200/byteabyteiguaisàmain. Verdeantigo ainda público. Candidato atualizado exatamente main+duascoresCSS; scripts/copy/links/controle iguais àmain, alegação20.000 preservada mas não comprovada. NodeVMigualdadehref/constante+10casoscomportamentaisPASSemprodução/proposta; delay150ms/Lead antesdenavegação normal,semrede. Chromiumreal390×844/360×800/320×740/1280×900 baseline/candidato: semoverflowhorizontal/fotoquebrada/JSexception;CTAmesmageometria,inteiro na primeiradobra390/360;scrollnativo,foco+Enter validados com timer interceptado sóQA. Screenshotsatualizados inspecionadosvisualmente,CTAescuro/textoemduaslinhaslegível,semcorte. NãoSafari real/WebVitals/ganhoCVR; nenhumLeadreal/joinWhatsApp. Falha inicialdeautodescoberta dobrowser resolvida com endpointCDP explícito existente,semreiniciar browser/serviços/outrosperfis. Falha inicialhelper poroperational-probeausente corrigida comcoleta real,saída preservada.

![CRO-002 atualizado — 390×844, não publicado](cro/screenshots/CRO-002-sync-2026-11-15-390x844.png)

**Gate e plano:** removido gateGitHub401 após identidade/permissão e readback remoto da sincronização; permanece **decisão humana ibombonato no#16** e posterior confirmaçãoPagesSHA+HTML. Após publicar: congelar14dias completos anteriores/excluir dia misto/revalidar uma vez referência4170conformeplano, incluir fases de targeting/clone como contexto/sensibilidade sem trocar métrica primáriaCVR/CPLsecundária. Não faltamLPVdoCRO-001 nemmaterialparacontraste. BL-02ICE8/5/8 compactaçãoúnica continua próximo fallback sem material, não implementarjunto; pedidos23/outdeofertasreais e comprovação20.000/estrelas03/nov pendentes, semcobrançarepetida. Próximaobservação16/nov09hSP inclui15/nov, primeirodia completo após novas mudançasMeta; checar decisão#16/publicação/mix/revisões.

**Operação separada:** execução14/nov991d210f191444b6a5810a026f47a90ccompleted,ponteTelegramrecibo20456às12:10:17Z,ID/handle/SHA256darespostafinalextraídaconferidos. A falha23/out não éestadoatual; recibodehoje só após conclusão, semenviodireto. Nenhumaagenda/credencial/serviço/outroperfilalterado. Artefatosatuaisem ~/work/hermes-scratch/cro-icb-2026-11-15/, rawsMCP/Graph, external-exposure-audit.json, QA/capturas, history-read-validation.json e readbackremoto; nunca confundir push doPR com publicação.


## Acompanhamento diário — 2026-11-16

**Decisão/entrega concreta:** CRO-002 **Em PR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out preservado/reconsultado sem revisão, não reaberto. [Primeiro dia completo do clone/targeting e guard do próximo teste](cro/research/2026-11-16-first-full-day-clone-and-control-phase.md): conciliação MCP/Graphdiário+horário/ad-day do clone, configuração de todos os anúncios comparada e planoBL-02 refinado sem pooling de campanhas. Nenhuma nova hipótese implementada/ID/PRparalelo. AutenticaçãoGitHubHTTP200/identidadeibombonato/permissãopush seguem válidas; atualizar mesmoPR#16 com diário dehoje e main atual mantendo apenas duas coresCSS como tratamento. Gate restante é **decisão humana ibombonato no#16**, seguido de confirmaçãoPagesSHA+HTML; não falta volumeCRO-001/material para contraste.

**Fontes:** snapshot principal 2026-11-16T12:04:03.766720+00:00; main/histórico integralPR#16/versões dos demaisPRs pendentes lidos ou comprovados como main/prefixo do histórico lido; PRs abertos/fechados e commits consultados. Worktree isolada, todos registros e recursos anteriores preservados. MCPoficial inicializado/protocolo2025-11-25 negociado/reutilizado,schemas/conta consultável/campos confirmados; quatro janelas conciliadas exatamente emgasto/impressões/cliques/LPV/Leads com GraphGET diário29/set–15/nov, aliases selecionados, atribuição unificada preservada, paginação/continuações concluídas. Anúncios/device/placement eentrega diária/horária reconciliados; resíduos monetários inferiores a1centavo sem relaxar contagens/totaisprincipais.16/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado; baseline histórico36% semdenominador somente descritivo.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-15–2026-11-15|Experimental|R$155,49|20680|680|555|212|38,20%|R$0,73|
|1|2026-11-15–2026-11-15|Controle|R$145,04|20507|629|535|227|42,43%|R$0,64|
|3|2026-11-13–2026-11-15|Experimental|R$453,54|61305|2061|1673|627|37,48%|R$0,72|
|3|2026-11-13–2026-11-15|Controle|R$444,08|67883|1828|1539|591|38,40%|R$0,75|
|7|2026-11-09–2026-11-15|Experimental|R$1030,59|145173|4836|3950|1404|35,54%|R$0,73|
|7|2026-11-09–2026-11-15|Controle|R$1020,76|169181|4475|3786|1403|37,06%|R$0,73|
|14|2026-11-02–2026-11-15|Experimental|R$2098,84|328760|10462|8632|3044|35,26%|R$0,69|
|14|2026-11-02–2026-11-15|Controle|R$2084,66|427606|10125|8486|3137|36,97%|R$0,66|

**Novidade desde ontem:** primeiro dia inteiro das condições externas de14/nov,15/nov: experimental38,20%(+1,85p.p.),controle42,43%(+7,83p.p.); diferença diária−4,23p.p.,IC95%nominal−10,05a+1,59.7d diferença−1,51p.p.,IC95%−3,66a+0,63;14d−1,70p.p.,IC95%−3,14a−0,26, não causal após múltiplasleituras/campanhasdistintas/eventosatribuídos/dependentes/mix. Semanas02–08→09–15/nov: experimental35,03→35,54% (0,52p.p./1,47%relativo);controle36,89→37,06% (0,16p.p./0,44%); diferença entre evoluções relativas1,03pontospercentuais. Nenhuma taxa medeCRO-002não publicado. Revisão14/novcontroleR$154,94→154,95/impressões24024→24025;LPV/Leadsinalterados,snapshots preservados. Novosads21/out510LPV/199Leads=91,89%dosLPVexperimentais. Incidente28/outpreservado/causaoriginaldesconhecida,15/novnão repetequasezero.

**Clone separado:**120252642171330505,15/novR$57,13/7803impressões/252cliques/207LPV/81Leads=39,13%,CPLR$0,71,Wilson95%32,74–45,92. Adprincipal206LPV/81Leads e segundo1LPV/0Lead; não julgar segundo pela amostra1/nem supor50/50. Todos ads/conjuntos/campanha do clone idênticos ao readback deontem,doisativos apontam explicitamenteindex3,ACTIVE/R$50dia. OriginaisACTIVE/R$150cada econfiguração/copy/destinos/UTMs/tracking/atribuição iguais; controle preserva targeting editado14/nov,semcausaCVRcomprovada. Única diferença bruta nos originais miniaturaassinadadoantigoPAUSED;41atividades desde14/nov/paginaçãoesgotada,nenhuma nova relevante após15/nov00h;4draftsidênticos. **Não somar clone ao endpointoriginal, não inferir coortes únicas/canibalização/lift.** Handoffgestoribombonato: considerar exposição compartilhada ealocação desigual como contexto, sem alterarMeta. BL-02ICE8/5/8 refinado com resultadooriginal exclusivo/sérieclone separada/fasecontrole/durações corretas,sensibilidades semredefinirendpoint ou novo gate. Pedidos23/out/comprovação20.000/estrelas03/novpendentes,semcobrançarepetida.

**Publicação e QA da sincronização:** humanos integraram#47/#48/#49/#50; diff daslandings desdea98cb83 somenteURLsdeconvite, não texto/CTA/Pixel/handler;#50 éindex.html fora dofunil. Pagesdeployment7823329119success16/nov11:58:54Z/Actions43862346727success paraSHA4dcf7ffe175e10e59db2cd53241d0ba8199d2db3;ambosHTMLsHTTP200/byteabyteiguaisàmain. Verdeantigo ainda público. Integração localmain+head#16 preservou links/conteúdo20.000não validado econtrole; candidatoexatamentemain+duascoresCSS. NodeVMigualdadehref/constante+10casoscomportamentaisPASSemprodução/candidato,Lead antesdenavegação/delay150ms,semrede. Chromiumreal390×844/360×800 capturados einspecionadosvisualmente: CTAlegívelduaslinhas/inteiro primeiradobra,mesmageometria503,75–565,75/500,14–560,14px;semcortes/overflow/fotoquebrada/JSexception,scroll/focoEnterPASS,extras320×740/1280×900PASS. Meta/WhatsAppbloqueadosantesdenavegar,interceptaçõessóQA,zeroLeadreal/join/mensagem. NãoSafari/WebVitals/lift. Falhasiniciaisexecute_code/terminal-cbloqueadas semexecução; fluxo final comarquivoshelperspermitidos,semalteraraprovações. Atualização da branch não equivale apublicação; readbackremote-sync-verification.json condiciona confirmação do envio.

![CRO-002 sincronizado, não publicado — 390×844](cro/screenshots/CRO-002-sync-2026-11-16-390x844.png)

**Plano/gate/próxima observação:** decidir#16; sóapóspublicaçãoPagesSHA+HTMLcongelar14diascompletosanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. PrimáriaCVR/CPLsecundária,checkpointvolume+coberturasemanal/consistência;semaguardar significância indefinidamente.17/nov09hSPinclui16/novcompleto,segunda jornada inteira após lançamentoclone/targeting;checar decisão/publicação,mix/alocaçãoclone/atribuição. NenhumCROnovo/merge/auto-merge/deploy/mutaçãoMeta.

**Operação separada:** execução15/nov48b9e7c2ad074c80811fe5f81d7476accompleted,ponteTelegramrecibo20531às12:16:02Z;ID/handle/SHA256darespostafinalextraídaconferidos. Falha23/outnãoéestadoatual. Schedulerhostservindorich-conversion/heartbeatativo/próximarotina17/nov12hUTC verificados,nãomodificados. Recibodehoje sóapósconclusão,semenviopróprio. Nenhumaagenda/serviço/credencial/outroperfilalterado. Artefatosatuaisem ~/work/hermes-scratch/cro-icb-2026-11-16/.


## Acompanhamento diário — 2026-11-17

**Estado/entrega concreta:** CRO-002 **Em PR#16, não publicado**; CRO-001 encerrado **Inconclusivo**, endpoint14–21/out preservado, sem revisão de LPV/Leads/gasto e sem reabrir. [Nova edição de público do clone e guard de fases](cro/research/2026-11-17-clone-interest-change-and-phase-guard.md): interesse O Boticário acrescentado externamente ao OR em16/nov13:51:21SP; comparação porID confirma mesmos ads/criativos/status finais. Reordenamento da resposta não foi confundido com troca de anúncios. BL-02ICE8/5/8 refinado com proveniência de targeting/OR/AND e fase15/nov versus16/novmisto versus17/novcompleto, sem implementar tratamento paralelo ou mudar endpoint. **Gate: ibombonato decidir#16, depois confirmarPagesSHA+HTML**, não esperar maisCRO-001/material para contraste.

**Dados:** MCP oficial inicializado, protocolo negociado reutilizado, schemas/conta consultável/campos verificados; quatro janelas conciliadas exatamente emgasto/impressões/cliques/LPV/Lead com GraphGET diário29/set–16/nov; aliases selecionados, atribuição unificada preservada, paginação/continuações concluídas. Anúncios/device/placement/entrega horária conciliados; contagens/totaisprincipais exatos, resíduos monetários inferiores a1centavo permitidos só nos breakdowns. Snapshot2026-11-17T12:02:47.680542+00:00;17/novparcial excluído. **Lead=proxy de clique antesdenavegar, não participante confirmado. Baseline histórico36%, semdenominador, referência descritiva.**

|Dias|Período inclusivo São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-16–2026-11-16|Experimental|R$183,15|29514|877|715|244|34,13%|R$0,75|
|1|2026-11-16–2026-11-16|Controle|R$179,97|26399|693|581|240|41,31%|R$0,75|
|3|2026-11-14–2026-11-16|Experimental|R$497,46|71787|2284|1878|677|36,05%|R$0,73|
|3|2026-11-14–2026-11-16|Controle|R$479,96|70931|1943|1642|649|39,52%|R$0,74|
|7|2026-11-10–2026-11-16|Experimental|R$1070,86|152176|4961|4031|1423|35,30%|R$0,75|
|7|2026-11-10–2026-11-16|Controle|R$1055,85|167186|4416|3727|1398|37,51%|R$0,76|
|14|2026-11-03–2026-11-16|Experimental|R$2097,09|327453|10432|8581|3007|35,04%|R$0,70|
|14|2026-11-03–2026-11-16|Controle|R$2085,43|402979|9811|8236|3060|37,15%|R$0,68|

**Desde ontem/incerteza:** experimental38,20→34,13% (-4,07p.p.),controle42,43→41,31% (-1,12p.p.). Diferença diária−7,18p.p.,IC95%nominal−12,48a−1,88;7d-2,21p.p.,IC95%-4,35a-0,07. Exclusão nominal dezero após múltiplasleituras/campanhas distintas/eventosatribuídos/dependentes não prova causa ou derrota de tratamento não publicado. Semanas03–09→10–16/nov:experimental34,81→35,30% (1,40%relativo);controle36,86→37,51% (1,76%);diferençaentre evoluçõesrelativas-0,36pontospercentuais. Sem revisões dosdiascomuns versuscoleta16/nov. Novosads21/out678LPV/233Leads=94,83%dosLPVoriginais. Incidente28/outpreservado/causaoriginaldesconhecida;16/novnão repetequasezero.

**Exposição externa:** clone separado211LPV/66Leads/R$58,41=31,28%,CPLR$0,885;16/novmistoapósinteresseO Boticárioadicionado. Configuraçõesoriginais inalteradas,controle mantém targeting14/nov,orçamentosR$150cada;cloneR$50.52atividadespaginadas,quatrodraftsidênticos. Não somar clone/assumircoortesúnicas ou atribuirquedaàediçãointradiária. Gestoribombonato deve considerar fases registradas,semrecomendação demutaçãoMeta. Materiais23/out/comprovação20.000/estrelas03/novpendentes,semcobrançarepetida.

**Publicação/sincronização:** humanos integraram#51/#52/#53, ambaslandings diferem davéspera somenteURLsdosconvites; não reiniciambaseline. Main1937ec89058aa8a872e84f7e9ebd98bad1fa537d,deployment7849001917success2026-11-17T09:16:44Z/Actions44054009257success;ambosHTMLsHTTP200/byteabyteiguaisàmain,coresantigaspublicadas. Histórico integral main e versões dosPRs abertos lidos ou conferidos como prefixos; todos registros anteriores preservados. AutenticaçãoGitHubHTTP200/ibombonato/pushconfirmados. Sincronizar mesmo#16 com mainatual e diário,tratamento apenasduascoresCSS,controle/scripts/copy/URLs preservados. NodeVMigualdadehref/constante+10casosPASSemprodução/proposta;Chromium390×844/360×800 capturados einspecionados:CTAinteiro/legívelduaslinhas,geometria igual,semoverflow/cortes/JSexception,foto/seisbenefícios/scroll/focoEnterPASS;extras320/1280PASS. DomíniosMeta/WhatsAppbloqueadosantesdenavegar,interceptaçõessóQA,zeroLeadreal/join/mensagem. NãoSafari/WebVitals/lift. Alegação20.000preservada,não validada. Readbackremoto condiciona confirmação doenvio.

![CRO-002 atualizado, não publicado —390×844](cro/screenshots/CRO-002-sync-2026-11-17-390x844.png)

**Próxima observação:**18/nov09hSP inclui17/novcompleto,primeirodia inteiro do targetingnovo doclone;verificar decisão#16/PagesSHA+HTML,mix/revisões semalterarprimária. Sóapóspublicação congelar14dias completosanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. NenhumCROnovo/PRparalelo/merge/auto-merge/deploy/Metaeditado. Operação16/novconcluída execução6456eb0c53c0451083a2c20533f01368,reciboTelegram20595às12:11:02Z/hashdarespostaextraídaconferido;falha23/outnãoéestadoatual. Schedulerhost/heartbeat/próximarotina18/nov12hUTCverificados,nãomodificados. Recibodehojesóapósconclusão,semenviodireto/outrosperfisalterados. Artefatos em ~/work/hermes-scratch/cro-icb-2026-11-17/.


## Acompanhamento diário — 2026-11-18

**Decisão/entrega concreta:** CRO-002 **Em PR#16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out preservado, sem reabrir. [Mudanças externas publicadas e guard de fases](cro/research/2026-11-18-external-creative-targeting-publication-and-phase-guard.md): público/copy original alterados e novo conjuntoAdvantage+ do clone confirmados porGraph+atividades, não por mero desaparecimento de drafts. BL-02ICE8/5/E8 refinado com versão de criativo porID e séries de conjunto separadas; nenhum tratamento paralelo/IDnovo. Gate: **ibombonato decidir#16, depois confirmarPagesSHA+HTML**, não volumeCRO-001/material.

**Fontes:** histórico integral main/PRpendente lido, versões dos demais PRs confirmadas como main/prefixos; PRs abertos/fechados/commits inspecionados. MCP oficialread-only/protocolo2025-11-25 negociado/schema/conta/campos confirmados, mesma conversa/sessão, paginação/continuações concluídas. Quatro janelas reconciliadas exatamente comGraphGET diário29/set–17/nov emgasto/impressões/cliques/LPV/Lead; aliases selecionados, atribuição unificada preservada.18/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado. Baseline histórico36% semdenominador apenas descritivo.**

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-17–2026-11-17|Experimental|R$144,12|22279|688|574|190|33,10%|R$0,76|
|1|2026-11-17–2026-11-17|Controle|R$151,39|20670|596|495|160|32,32%|R$0,95|
|3|2026-11-15–2026-11-17|Experimental|R$482,78|72474|2245|1844|646|35,03%|R$0,75|
|3|2026-11-15–2026-11-17|Controle|R$476,41|67577|1918|1611|627|38,92%|R$0,76|
|7|2026-11-11–2026-11-17|Experimental|R$1071,34|154466|4968|4036|1410|34,94%|R$0,76|
|7|2026-11-11–2026-11-17|Controle|R$1069,46|163042|4350|3660|1373|37,51%|R$0,78|
|14|2026-11-04–2026-11-17|Experimental|R$2083,91|315013|10083|8307|2929|35,26%|R$0,71|
|14|2026-11-04–2026-11-17|Controle|R$2089,68|373713|9431|7936|2944|37,10%|R$0,71|

**Desde ontem:** CVRexperimental34,13→33,10%;controle41,31→32,32%. Diferença7d-2,58p.p.,IC95%nominal-4,73a-0,43; semanas04–10→11–17/nov:experimental35,57→34,94%(-1,77%relativo),controle36,74→37,51%(2,11%); diferença entre evoluçõesrelativas-3,88pontos percentuais. Observacional/eventosatribuídos/dependentes/campanhasdistintas/leituras sequenciais; nenhum resultado do contraste não publicado. Revisões16/nov:original+R$0,02/+1impressão,controle+R$0,01/+1impressão;clone+R$0,13/+21impressões/+2cliques,LPV/Leadinalterados. Snapshots preservados.

**Nova exposição externa:** original em17/nov18:43:10SP faixa configurada24–50→22–45/mobile→mobile+desktop; criativos substituídos nosads120251541120490505 e120252297350870505, primeiro agora2→7bodiesativas. Links/UTMs/Pixeldeconversão mantidos, referências de post nos tracking_specs mudaram com os criativos, não declarar tracking inteiro idêntico. Controle sem nova edição. Orçamentos atuais150/150/clone50. Drafts4→0, mas publicação deriva dos camposlive/atividades; não presumir que todos antigos drafts foram aplicados integralmente. Clone ganhou conjunto120252802517710505/AdvantageAudience1/faixa22–65 e3ads(doisACTIVE/umPAUSED); primeiraentrega17/nov18:55:59SP, segundoativo18/nov02:32:18SP.101atividades paginadas,IDs inacessíveis preservados como limitação, sem inferir gasto oculto. **Gestoribombonato: considerar publicações e fases na leitura, não editarMeta por conta do agente.**

**Clone separado/qualidade:** conjunto original do clone em17/nov,primeiro dia inteiro apósO Boticário:178LPV/71Leads/R$42,63=39,89%,CPLR$0,60. Novo conjunto parcialR$2,05/0LPV/0Lead, semCVRestimável. Campanha178/71/R$44,68 conciliada exatamente porMCP/dia/anúncio/conjunto/horas; **breakdownsdevice/posição somamR$44,67,resíduo−R$0,01 persistente apósreconsulta:gate monetárioFAIL,contagensexatas**, não tolerância relaxada. Revisãointrarodada44,67→44,68 preservada. Comparação conjuntooriginal17vs15/nov+0,76p.p.,IC95%−9,04a+10,55,semganhocausal. Não somarcloneaoendpointoriginal.17/nov misto original/clone preservado,18/nov primeirodia completo dasnovascondições,sem reiniciarCROouinventar esperaextra.

**Publicação/QA/sincronização:** humanos integraram#54/#55,somenteconvites,verificação deHTMLnormalizado apenasURLsPASS. Main`f832c604717680495d55311225dd5b4b206820ef`,deployment7872323102success2026-11-18T02:28:49Z/Actions44223463709success;ambosHTMLsHTTP200/byteabyteiguaisàmain,coresantigaspublicadas. Integração main+head#16exatamente2coresCSS,controle/scripts/copy/URLs preservados,alegação20.000não validada. NodeVMigualdadehref/constante+10casoscomportamentaisPASSemprodução/proposta. Chromium390×844/360×800 capturados/reinspecionados:CTAlegívelinteiro/duaslinhas,mesmageometria503,75–565,75/500,14–560,14;semoverflow/corte/exceçãoJS,foto/seisbenefícios/scroll/focoEnterPASS,extras320/1280PASS. Meta/WhatsAppbloqueadosantesdenavegar,interceptaçõessóQA,zeroLeadreal/join/mensagem. NãoSafari/WebVitals/lift. HelperGitHubinicial404porbarratraseira corrigidosomente naURLdaAPI,semalterarcredenciais;identidade/permissãopushconfirmadas. Atualizar mesmo#16,readbackremoto obrigatório antesdeafirmarenvio.

![CRO-002 atualizado, não publicado —390×844](cro/screenshots/CRO-002-sync-2026-11-18-390x844.png)

**Próxima observação:**19/nov09hSãoPaulo inclui18/novcompleto: público/copy original e novo conjunto do clone,controle e atribuição;decisão#16 ePagesSHA+HTML. Sóapóspublicação congelar14diasanteriores/excluir diamixto/revalidaruma vez4170conformeplano,semseleção favorável. Materiaisautorizados/comprovação20.000/estrelas continuam pendentessemnovacobrança. Operação17/novconcluída execuçãod0d664aa30bc4c10a60884b8e9096b12,Telegramrecibo20715às12:11:01Z/hashdarespostafinalextraídaconferido;falha23/outnãoéestadoatual,incidente resolved. Entregadehoje sóapósconclusão,semenviodireto/agendamento/outrosperfisalterados. Artefatosscratch2026-11-18;semMetaeditado/controlealterado/merge remoto/auto-merge/deploy.


## Acompanhamento diário — 2026-11-19

**Decisão/entrega concreta:** CRO-002 **Em PR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out fechado. [Fronteira de pausas e roteiro qualitativoBL-03](cro/research/2026-11-19-pause-phase-and-comprehension-protocol.md): duas pausas externas posteriores ao cutoff diagnosticadas, plano porfase/ID preservado e roteiro não indutivo de compreensão preparado (não aplicado; ICEI6/C4/E8, sem confiança emlift aumentada). Nenhum tratamento paralelo/novoIDCRO. Gate **ibombonato decidir#16 e confirmar publicaçãoPagesSHA+HTML**, não volumeCRO001/material opcional.

**Dados atuais:** MCP oficial read-only/schemas/conta/campos/protocolo negociado2025-11-25, mesma sessão/conversa; quatro janelas reconciliadas exatamente comGraphGETdiário29/set–18/nov emgasto/impressões/cliques/LPV/Lead.135verificações, contagensbreakdowns exatas/resíduo monetário máximoR$0,000001, paginação/continuações concluídas.19/novparcial excluído. **Lead=proxyclique pré-navegação, não participante. Baseline histórico36%semdenominador, descritivo.**

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-18–2026-11-18|Experimental|R$144,07|24930|681|561|192|34,22%|R$0,75|
|1|2026-11-18–2026-11-18|Controle|R$134,08|17078|568|468|174|37,18%|R$0,77|
|3|2026-11-16–2026-11-18|Experimental|R$471,37|76725|2246|1850|626|33,84%|R$0,75|
|3|2026-11-16–2026-11-18|Controle|R$465,45|64149|1857|1544|574|37,18%|R$0,81|
|7|2026-11-12–2026-11-18|Experimental|R$1068,48|158282|4990|4075|1427|35,02%|R$0,75|
|7|2026-11-12–2026-11-18|Controle|R$1056,84|155187|4313|3611|1363|37,75%|R$0,78|
|14|2026-11-05–2026-11-18|Experimental|R$2126,46|323235|10207|8407|2937|34,94%|R$0,72|
|14|2026-11-05–2026-11-18|Controle|R$2112,27|363738|9370|7868|2927|37,20%|R$0,72|

**Desde ontem/incerteza:**18/novCVR34,22%/37,18%;7ddiferença−2,73p.p.,IC95%nominal−4,88a−0,57. Semanas05–11→12–18/nov:experimental34,86→35,02%(+0,46%relativo),controle36,74→37,75%(+2,74%);diferençaentre evoluçõesrelativas−2,28pontospercentuais,entre mudanças−0,84p.p.(IC95%−3,80a+2,11). Não causal/campanhasdistintas/mix/eventosatribuídos/dependentes/leituras sequenciais;nenhum resultadoCRO002não publicado. Revisões17/nov:originalR$144,12→144,13/22279→22280impressões;controle20670→20671;cloneR$44,68→44,74/8418→8425. LPV/Leadinalterados,snapshots preservados. Gate monetárioclone17/nov passa na reconsulta atual;FAIL anterior não apagado.

**Mudança externa:**ads120250848857170505 e120252297350880505 pausados19/nov00:08:34/00:08:37SP,agora2ACTIVE/3PAUSED;108atividades/paginaçãoesgotada. Pausas após18/nov, não explicam retrospectivamente seuresultado nem apagam histórico. Doisativos apontamindex3,copy/criativos/destinos/UTMs/atribuição iguaisàcoleta18/nov;controleumativo/index4_li,orçamentos150/150/clone50semnovaedição. Clone18/nov239LPV/72Leads/R$52,65=30,13%;conjuntonovo136LPV/original103,sem50–50/pooling/coortesúnicas. Responsávelibombonato:considerarfronteira19/nov,versõescriativas17/novecontrole14/nov;agente não alterouMeta.

**Publicação/QA/sincronização:** histórico integralmain/PR16 lido, versõesdosdemaisPRsconferidasmain/prefixos;PRsabertos/fechadosecommitsinspecionados. Novas rotações#56–#60 naslandings medidas somenteURLs,HTMLnormalizadoPASS. Main`10c764b2ec92daf71d63f3b8067b17202d700a50`,deployment7912203791success2026-11-19T11:48:34Z/Actions44518002031success;ambosHTMLsHTTP200/byteabyteiguaisàmain,contrasteantigo público. Integraçãolocalmain+head#16exatamente2coresCSS,controle/scripts/copy/URLsatuaispreservados;20.000/estrelasnão validados. NodeVMigualdadehref/constante+10casosPASSemprodução/candidato. Chromium390×844/360×800capturados einspecionadosvisualmente:CTAinteirolegívelduaslinhas/mesmageometria,semoverflow/corte/JSexception,foto/seisbenefícios/scroll/focoEnterPASS;extras320/1280PASS. Meta/WhatsAppbloqueadosantesdenavegar,zeroLeadreal/join/mensagem. Helperantigoactivate_tabinexistente corrigidoparaswitch_tab/Target.closeTargetconforme runtime lido,semreinstalação. NãoSafari/WebVitals/lift.

![CRO-002 sincronizado, não publicado —390×844](cro/screenshots/CRO-002-sync-2026-11-19-390x844.png)

**Próxima observação:**20/nov09hSãoPaulo,dados19/novcompleto,primeirodiaapósduaspausas;preservarsérieoriginal/fases/clone separado,checardecisão#16ePagesSHA+HTML. Sóapóspublicação congelar14diasanteriores/excluirdiamixto/revalidarumavez4170conformeplano;semnovo gatearbitrário. Pedidosmateriais/comprovaçãosocialseguempendentessemrepetir. Operação18/novcompleted `3a818bc2b84341739a39e9a293f2c47d`,Telegramrecibo20799às12:21:01Z/hashdarespostaextraídaverificado;incidente23/outresolved,nãofalhaatual. Entregadehojeaindapendente atéconclusão,sem enviopróprio/agendamento/configuração/outrosperfisalterados. Artefatos scratch2026-11-19. AtualizaçãomesmoPR16/readbackremotoobrigatório;semmerge/auto-merge/deploy/Metaeditado.

## Acompanhamento diário — 2026-11-20

**Decisão/entrega concreta:** CRO-002 **Em PR#16, não publicado**; CRO-001 continua **Inconclusivo**, endpoint14–21/out fechado. [Fronteira das pausas e guard do próximo teste](cro/research/2026-11-20-pause-boundary-and-next-test-guard.md): 19/nov reconciliado poranúncio, exposição residual dos pausados preservada e BL-02 refinado com proteção contra seleção retroativa porstatus. ICE8/5/8 mantido; nenhum tratamento paralelo/novoIDCRO. Gate: **ibombonato decidir#16; depois confirmarPagesSHA+HTML**. Não faltamLPVdoCRO001 oumaterial opcional.

**Fontes:** histórico integralmain/PR16 lido, versões dosoutrosPRs pendentes comprovadas comomain/prefixos; PRs abertos/fechados/commits conferidos. MCPoficial read-only inicializado/protocolo2025-11-25 negociado, schemas/conta/campos verificados; mesma sessão/conversa, paginação/continuações concluídas. 140reconciliaçõesPASS,1/3/7/14dias exatos emgasto/impressões/cliques/LPV/Lead versusGraphGETdiário29/set–19/nov; contagensbreakdowns exatas/resíduo monetário máximoR$0,000001.20/novparcial excluído. **Lead=proxy de clique pré-navegação, não participante confirmado. Baseline histórico36%semdenominador, descritivo.**

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques link|LPV|Leads proxy|CVR|CPL proxy|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-19–2026-11-19|Experimental|R$154,10|29018|727|588|212|36,05%|R$0,73|
|1|2026-11-19–2026-11-19|Controle|R$149,94|20862|531|444|184|41,44%|R$0,81|
|3|2026-11-17–2026-11-19|Experimental|R$442,30|76228|2096|1723|594|34,47%|R$0,74|
|3|2026-11-17–2026-11-19|Controle|R$435,41|58611|1695|1407|518|36,82%|R$0,84|
|7|2026-11-13–2026-11-19|Experimental|R$1079,01|167048|5034|4111|1465|35,64%|R$0,74|
|7|2026-11-13–2026-11-19|Controle|R$1059,47|152894|4216|3527|1349|38,25%|R$0,79|
|14|2026-11-06–2026-11-19|Experimental|R$2107,70|323661|10055|8264|2881|34,86%|R$0,73|
|14|2026-11-06–2026-11-19|Controle|R$2095,89|346586|9056|7609|2850|37,46%|R$0,74|

**Desde ontem/incerteza:** experimental34,22→36,05%,controle37,18→41,44%; diferença diária−5,39p.p.,IC95%nominal−11,39a+0,62.7ddiferença−2,61p.p.,IC95%−4,78a−0,44. Semanas06–12→13–19/nov:experimental34,10→35,64%(+4,52%relativo),controle36,77→38,25%(+4,02%); diferençaentre mudanças+0,06p.p.,IC95%−2,93a+3,06. Comparações observacionais/campanhasdistintas/eventosatribuídos/dependentes/leituras sequenciais; nenhum resultado do contraste não publicado. Originais sem revisões versusontem; clone18/nov gasto52,65→52,77,impressões10818→10854,cliques303→305,LPV/Leadinalterados,snapshots preservados.

**Entrega analítica nova:** pausas19/nov00:08:34/00:08:37SP deixam8min37s anteriores àúltimapausa no dia19;20/nov é primeiro dia civil inteiramente posterior, ainda incompleto. Par pausado registrouR$0,03/5impressões/zeroLPV/Lead em19, não zerar história nem inferir horário individual dasimpressões. Mesmos doisIDs sobreviventes18→19:176/502=35,06%→212/588=36,05%,Δ+0,99p.p.,IC95%−4,70a+6,69,contra+1,83p.p.agregado. Realocação277→95LPV e225→493LPV impede confundir IDsconstantes com distribuição constante. BL-02ICE8/5/8/compactaçãoúnica preservado; novo guard mantémTODOSoshistoricamenteveiculados noprincipal, cobertura/IDs/célulasvazias e dias mistos explícitos, sensibilidade secundária semseleção porstatus/p-valor. Nenhuma nova mudança semântica dehierarquia/configuração versusontem;110atividadespaginadas,0novasrelevantes;2ACTIVE/3PAUSEDoriginal/1ACTIVEcontrole/4ACTIVEclone,orçamentos150/150/50,drafts0. Clone19/nov223LPV/65Leads/R$48,34=29,15%,sempooling/coortesúnicas. Handoffgestoribombonato: considerar fases externas14/17/19nov,nenhumaediçãoMeta peloagente.

**Publicação/QA/sincronização:** main`4ec19e3ea31a7053bb4a78efa2a6a481c0f09e08`,deployment7940611961success20/nov11:36:39Z/Actions44728901326success;ambosHTMLsHTTP200/byteabyteiguaisàmain,contrasteantigo público. Nova rotação humana#61 sóURLscontrole;normalizaçãoURLsPASS,nãoreiniciabaseline. Integração main+head#16 exatamente2coresCSS,index4_li/scripts/copy/URLsatuaispreservados;20.000/estrelasnão validados. NodeVMigualdadehref/constante+10casosPASSemprodução/candidato. Chromium390×844/360×800capturados einspecionadosvisualmente:CTAinteirolegívelduaslinhas/mesmageometria503,75–565,75/500,14–560,14,semoverflow/corte/exceçãoJS,foto/seisbenefícios/scroll/focoEnterPASS;extras320/1280PASS. Meta/WhatsAppbloqueadosantesdenavegar,zeroLeadreal/join/mensagem. NãoSafari/WebVitals/lift. AutenticaçãoGitHubHTTP200/identidadeibombonato/permissãopushconfirmadas; atualizar mesmo#16,readbackremoto obrigatório antesdeafirmar envio.

![CRO-002 sincronizado, não publicado —390×844](cro/screenshots/CRO-002-sync-2026-11-20-390x844.png)

**Próxima observação:**21/nov09hSãoPaulo,dados20/novcompleto,primeirodia civil integral após pausas,semseleção deendpoint;verificar decisão#16/PagesSHA+HTML/mix/atribuição/clone separado. Sóapóspublicação congelar14diasanteriores/excluir diamixto/revalidaruma vez4170conformeplano. Pedidosmateriais/comprovação20.000/estrelas continuam pendentes,semcobrançarepetida. Operação19/novcompleted`c2e7a612fdf14a9fb8c46b9e44782df2`eTelegramrecibo20947às12:20:43Z/hashdarespostaextraídaverificados;incidente23/outresolved,nãofalhaatual. Entregadehojesóapósconclusão,semenviodireto/agendamento/configuração/outrosperfisalterados. Artefatos scratch2026-11-20;semmerge/auto-merge/deploy/Metaeditado.

## Acompanhamento diário — 2026-11-21

**Decisão/entrega:** CRO-002 **Em PR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out fechado. [Primeiro dia integral após pausas e planoBL-02](cro/research/2026-11-21-first-full-postpause-day-and-next-test.md):20/nov reconciliado porID; mudança diária-2,09p.p.,IC95%[-7,85; 3,68]; composição0,10 e dentro-2,19p.p. Não há melhora operacional consistente comprovada nem autorização de editarMeta. ICEBL02 8/5/8 mantido, com regra contra baseline selecionado pela recuperação. Nenhum novoIDCRO/tratamento paralelo.

**Fontes:** história completa main/PR16 lida, versões dos outrosPRs comprovadas main/prefixos, PRs abertos/fechados e commits conferidos. MCPoficial read-only inicializado/protocolo2025-11-25, schemas/conta/campos, mesma sessão/conversa; 145 conciliaçõesPASS, totais1/3/7/14dias exatos versusGraphGET diário29/set–20/nov. Aliases selecionados, paginação/continuações concluídas.21/novparcial excluído. Lead=proxy de clique pré-navegação, não participante. Baseline36 sem denominador, descritivo. Helperinicial omitiu consulta clone19/nov;guard falhou, consulta feita hoje e verificação refeitaPASS, semcopiardadosantigos.

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques|LPV|Lead proxy|CVR|CPL|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-20–2026-11-20|experimental|R$127,83|20837|552|474|161|33,97%|R$0,79|
|1|2026-11-20–2026-11-20|controle|R$144,32|18175|559|468|178|38,03%|R$0,81|
|3|2026-11-18–2026-11-20|experimental|R$426,00|74785|1960|1623|565|34,81%|R$0,75|
|3|2026-11-18–2026-11-20|controle|R$428,34|56115|1658|1380|536|38,84%|R$0,80|
|7|2026-11-14–2026-11-20|experimental|R$1067,61|168853|4932|4075|1432|35,14%|R$0,75|
|7|2026-11-14–2026-11-20|controle|R$1059,70|147718|4197|3517|1345|38,24%|R$0,79|
|14|2026-11-07–2026-11-20|experimental|R$2105,31|323577|10010|8229|2877|34,96%|R$0,73|
|14|2026-11-07–2026-11-20|controle|R$2105,93|337150|8950|7526|2818|37,44%|R$0,75|

**Desde ontem/incerteza:**20/novCVR33,97%/38,03%.7ddiferença-3,10p.p.,IC95%nominal[-5,28; -0,93]. Semanas07–13→14–20/nov: experimental1,02%relativo/controle4,08%; diferençaentre mudanças-1,15p.p.,IC95%[-4,15; 1,86]. Campanhas distintas/eventosatribuídos/dependentes/mix/leituras sequenciais; não causal nem resultado do contraste ainda não publicado. Revisões versus20/nov preservadas emanalysis.json: []; clone:[{"date": "2026-11-19", "changes": {"spend": {"previous": "48.34", "current": "48.64"}, "impressions": {"previous": 9262, "current": 9320}, "clicks": {"previous": 279, "current": 280}}}].

**Exposição:**20/nov primeirodia civil inteiramente após pausas19/nov00:08SP; pausados sem entrega reportada hoje, mas histórico não removido. Nenhuma mudança semântica nova deconfiguração versusontem, somente miniaturaassinada noantigoPAUSED;112atividades paginadas/1novasrelevantes;drafts0. Clone separado20/nov:236LPV/83Leads/R$45,70,CVR35,17%; sempooling/coortesúnicas/canibalizaçãoinferida. Gestoribombonato deve considerar fases externas14/17/19nov,semalteraçãoMeta peloagente.

**Publicação/QA:**main127eb14fd0d31364d4519a6143472310ed927e72,deployment7956709874success2026-11-21T01:42:30Z/Actions44851693166success,ambosHTMLsHTTP200/byteabyteiguais,coresantigas. Rotaçãohumana#62 sóURLscontrole,normalizaçãoPASS,nãoreiniciaavaliação. Integraçãomain+head#16 exatamente2coresCSS,controle/scripts/copy/URLsatuaispreservados. Candidatoindex3 byteabyteidêntico ao auditado20/nov: semnova implementação visual,não repetir screenshots ou alegarQAvisualnova. Capturas390×844/360×800de20/nov continuam representativas;NodeVMigualdadehref/constante+10casosPASSemprodução/candidato,semrede/Leadreal/join. Alegação20.000/estrelasnão comprovada. AutenticaçãoHTTP200/ibombonato/pushconfirmados;atualizar mesmoPR,readback obrigatório.

**Gate/próximo:**ibombonato decidir#16;após publicação confirmadaPagesSHA+HTML congelar14diasanteriores/excluir diamixto/revalidaruma vez4170conformeplano. NãofaltamLPVdeCRO001/materialpara contraste. Próximaleitura22/nov09hSãoPaulo inclui21/novcompleto,mix/consistência/decisãohumana. Pedidosmateriais/comprovaçãosocial pendentes,semrepetição. Execução20/nov9c06234c4e954f27b3eb434e20e8eec9completed,Telegramrecibo21086/hashdarespostaextraídaverificados;incidente23/outresolvido,nãofalhaatual. Entregadehoje sóapósconclusão,semenviodireto/agendamento/configuração/outrosperfisalterados. Artefatos scratch2026-11-21;semmerge/auto-merge/deploy/Metaeditado.


**Nova atividade a esclarecer com gestor ibombonato:** first_delivery_event de20/nov19:08:36SP para ID120252802586720505, associado no extra_data ao conjunto clone120252802517710505. ID ausente da lista configurada; GET explícito retornouHTTP400/code100/subcode33 (inexistente, sem permissão ou operação não suportada, sem distinguir causa). Não inventar anúncio/criativo/destino/status, nem chamar de nova exposição identificada ou gasto oculto. Todas as contribuições ad-day retornadas conciliam exatamente a campanha; hierarchy atual semanticamente igual não resolve a identidade desse evento. Gestor deve confrontar o ID no histórico do AdsManager; sem ediçãoMeta pelo agente. Evidência emnew-first-delivery-object.json/expanded-activities.json.


## Acompanhamento diário — 2026-11-22

**Decisão/entrega:** CRO-002 **Em PR#16, não publicado**; CRO-001 permaneceInconclusivo, endpoint14–21/out fechado. [Rebote diário, cadeiaCPL e pacote de decisão](cro/research/2026-11-22-rebound-and-decision-packet.md): +6,63p.p.20→21/nov semnovo tratamento, composição0,54/dentro6,08p.p.; BL-02ICE8/5/8 refinado com caso deaceitação paraCVR/CPL divergentes. 30dias civis desde preparação do contraste: **ibombonato decidir#16**, não falta amostra oumaterial. Nenhum experimento paralelo/IDCROnovo.

**Fontes:** históricos integrais main/PR16 lidos, demaisPRs conferidos como main/prefixos; PRs abertos/fechados/commits consultados. MCPoficialread-only inicializado/protocolo2025-11-25, schemas/conta/campos,mesmasessão/conversa, paginação/continuações concluídas. 149conciliaçõesPASS, totais1/3/7/14dias exatos versusGraphGETdiário29/set–21/nov; aliases selecionados, atribuição unificada.22/novparcial excluído. Lead=proxycliquepré-navegação,não participante. Baselinehistórico36%semdenominador,descritivo. Falhasiniciais dehelper(missingclone20/fase14) preservadas;leiturasatuaisfaltantes executadas eguardrefeitoPASS,snapshotinicialpreservado,sem métricasantigascomosubstituto.

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques|LPV|Lead proxy|CVR|CPL|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-21–2026-11-21|experimental|R$141,13|25487|699|574|233|40,59%|R$0,61|
|1|2026-11-21–2026-11-21|controle|R$145,01|18954|597|518|204|39,38%|R$0,71|
|3|2026-11-19–2026-11-21|experimental|R$423,07|75346|1978|1636|606|37,04%|R$0,70|
|3|2026-11-19–2026-11-21|controle|R$439,27|57992|1687|1430|566|39,58%|R$0,78|
|7|2026-11-15–2026-11-21|experimental|R$1049,93|172751|4904|4041|1444|35,73%|R$0,73|
|7|2026-11-15–2026-11-21|controle|R$1049,76|142648|4173|3509|1367|38,96%|R$0,77|
|14|2026-11-08–2026-11-21|experimental|R$2099,82|326830|9963|8192|2914|35,57%|R$0,72|
|14|2026-11-08–2026-11-21|controle|R$2099,58|327141|8849|7462|2797|37,48%|R$0,75|

**Incerteza/novidades:**7ddiferença-3,22p.p.,IC95%nominal[-5,41;-1,04]. Semanas08–14→15–21/nov: diferençaentre mudanças-2,46p.p.,IC95%[-5,49;0,56],diferençaentre evoluçõesrelativas-6,78pontospercentuais. Comparaçõesobservacionais/eventosatribuídos/dependentes/mix/leituras repetidas,nãocausalidade nemresultado doCRO002não publicado. Revisõesversus21/nov preservadas emanalysis.json: original20/nov+R$0,01/+4impressões,controle+1impressão;clone20/nov+R$0,15/+45impressões/+2cliques,LPV/Leadiguais.

**Exposição:**semnova mudança semântica deconfiguração ouatividade relevante desdeontem;diferençabruta sóminiaturaassinadadoantigoPAUSED,drafts0. 2ativos/3pausadosoriginal,1ativocontrole,4ativosclone;orçamentos150/150/50. Clone separado21/nov192LPV/55Leads/R$40,03,CVR28,65%;sempooling/coortesúnicas. IDinacessível120252802586720505continua pendência jáencaminhada,nenhuma prova nova deidentidade/status ougastooculto. Fases14/17/19novmantidas;agente nãoalterouMeta.

**Publicação/QA:**mainbbdc31ad6da3cfd82861c52117cfd5e6363efc13,deployment7967349596success2026-11-21T18:12:38Z/Actions44934185314success,ambosHTMLsHTTP200byteabyteiguais,coresantigas. Rotaçãohumana#63somenteURLscontrole;#64operacionalpendente,nãoincorporado. Integraçãomain+head#16exatamente2coresCSS,controle/scripts/copy/URLsatuaispreservados;alegação20.000/estrelasnão validada. Candidatoindex3byteabyteidênticoàQAvisual20/nov;nenhumanovaimplementação,não alegarnovacaptura/Safari/WebVitals. NodeVMigualdadehref/constante+10casosPASSemprodução/proposta,semrede/Leadreal/join/mensagem. AutenticaçãoGitHubHTTP200/ibombonato/pushconfirmados;atualizarmesmoPR,readbackremotoobrigatório.

**Gate/próximaobservação:**ibombonatodecidir#16;depoisPagesSHA+HTML/congelar14diasanteriores/excluirdiamixto/revalidarumavez4170conformeplano. Próximaleitura23/nov09hSãoPaulo,dados22/novcompleto,consistênciadorebote/mix/decisãohumana. Pedidosmateriais/comprovação social pendentes,semnovacobrança. Execução21/novabfc7d087da44b9ab5dc1408ad19a33bcompleted,Telegramrecibo21167/hashdarespostafinalextraídaverificados;incidente23/outresolvido,nãofalhaatual. Entregadehojesóapósconclusão,semenviopróprio/agendamento/configuração/outrosperfisalterados. Artefatosscratch2026-11-22;semmerge/auto-merge/deploy/Metaeditado.


## Acompanhamento diário — 2026-11-23

**Decisão/entrega:** CRO-002 **Em PR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out fechado. [Sensibilidade pós-pausa e proteção do planoBL-02](cro/research/2026-11-23-postpause-composition-sensitivity.md): mesmos IDs18/nov→20–22/nov +3,27p.p., IC95%[-1,50;8,05], cobertura89,48%→100%; composição-2,34/dentro5,62p.p. Não comprova benefício de pausas/copy/landing. BL-02ICE8/5/8 refinado com gate de cobertura e fases, sem nova espera, ID ou tratamento. **ibombonato decidir#16** (31dias desde preparação); não falta amostra/material.

**Fontes:** históricos integrais main/PR16 lidos, demais pendentes iguais àmain/prefixos; PRs abertos/fechados, comentários/reviews e commits conferidos. MCPoficial read-only inicializado, protocolo2025-11-25,schemas/conta/campos,mesma sessão/conversa,paginação/continuações concluídas;156conciliaçõesPASS,MCP×GraphGETdiário,totais1/3/7/14exatos,aliases selecionados/atribuição unificada.23/novparcial excluído. Lead=proxycliquepré-navegação,não participante;baseline36%semdenominador apenas descritivo. Divergência intrarrodada clone22/nov resolvida por duas releituras atuais(segunda após60s),snapshots iniciais/falhas preservados,sem relaxar contagens/substituir métricas por antigas.

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques|LPV|Lead proxy|CVR|CPL|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-22–2026-11-22|experimental|R$169,48|34375|795|645|255|39,53%|R$0,66|
|1|2026-11-22–2026-11-22|controle|R$154,70|21437|666|566|218|38,52%|R$0,71|
|3|2026-11-20–2026-11-22|experimental|R$438,45|80704|2046|1693|649|38,33%|R$0,68|
|3|2026-11-20–2026-11-22|controle|R$444,03|58567|1822|1552|600|38,66%|R$0,74|
|7|2026-11-16–2026-11-22|experimental|R$1063,92|186447|5019|4131|1487|36,00%|R$0,72|
|7|2026-11-16–2026-11-22|controle|R$1059,42|143578|4210|3540|1358|38,36%|R$0,78|
|14|2026-11-09–2026-11-22|experimental|R$2094,51|331620|9855|8081|2891|35,78%|R$0,72|
|14|2026-11-09–2026-11-22|controle|R$2080,18|312759|8685|7326|2761|37,69%|R$0,75|

**Novidades/incerteza:**22/novCVR39,53%/38,52%;7ddiferença-2,37p.p.,IC95%nominal[-4,54;-0,20]. Semanas09–15→16–22/nov: diferença entre mudanças-0,85p.p.,IC95%[-3,90;2,20],entre evoluçõesrelativas-2,25pontospercentuais. Campanhas distintas/eventos atribuídos/dependentes/mix/leituras repetidas,não causalidade nem resultado do contraste não publicado. Revisõesversus22nov:original21nov+1impressão;clone21novR$40,03→40,12/9598→9625impressões,LPV/Leadiguais;originais preservados.

**Exposição:**sem mudança semântica nova deconfiguração/atividade relevante;somente miniaturaassinada doantigoPAUSED,drafts0. Original2ativos/3pausados,controle1ativo,clone4ativos/2pausados;orçamentos150/150/50. Destinos/copy/atribuição/dispositivo/posicionamento auditados;nenhum diagnósticoSafari inferido. Clone120252642171330505 separado22nov287LPV/80Leads/R$60,98,CVR27,87%;sem pooling/coortes únicas. Fases14/17/19nov e pendência jáencaminhada ID120252802586720505 preservadas,sem inventar identidade ou gastooculto.

**Publicação/QA:**main14c019a34b8f908412f6ccc1be03ddd18d5d6de2,deployment7986433374success2026-11-22T23:01:35Z,Actions45080870762success;ambosHTMLsHTTP200/byteabyteiguais,coresantigas. Humanos#64/#65alteraram sóURLscontrole;agente não alteroucontrole/rotas. Integração prospectiva main+head#16exatamente2coresCSS,copy/scripts/URLs/controle atuais preservados;provasocial20.000/estrelasnão validada. CandidatoidênticoàQAvisual20/nov,nenhuma nova implementação/captura/Safari/WebVitals alegada. NodeVMigualdadehref/constante+10casosPASS emprodução/proposta,semrede/Leadreal/join/mensagem. AutenticaçãoHTTP200/ibombonato/pushconfirmados;atualização mesmoPR sujeita areadback remoto.

**Gate/próximo:**ibombonato decidir#16;apóspublicação confirmarPagesSHA+HTML,congelar14diasanteriores/excluirdiamixto/revalidaruma vez4170conformeplano. Próximaobservação24nov09hSãoPaulo,dados23novcompleto,mix/atribuição/disposiçãohumana. Pedidosmateriais/comprovação social pendentes,semnovacobrança. Execução22novcb9a8172ebf2468b99e2a1757dc1bfe9completed,Telegramrecibo21265/hashdarespostafinalextraídaverificados;incidente23outresolved,nãofalhaatual. Entregahoje depende conclusão/recibo posterior,semenvio próprio nem alteração deagendamento/config/outrosperfis. Artefatosscratch2026-11-23;semmerge/auto-merge/deploy/ediçãoMeta.


## Acompanhamento diário — 2026-11-24

**Decisão/entrega:** CRO-002 **Em PR#16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out fechado. [Nova fase do clone e guardBL-02](cro/research/2026-11-24-clone-pause-and-next-test-guard.md): pausas externas23/nov19:49–19:50SP confirmadas; queda original22→23de-5,73p.p. tem composição poranúncio-0,01/dentro-5,72p.p.,cobertura100%;não prova causa. BL-02ICE8/5/8 refinado com tabelas separadas porcampanha/conjunto/fase,sem pooling, novoIDCRO outratamento. **ibombonato decidir#16** (32dias desdepreparação),não falta amostra/material.

**Fontes:** históricos integrais main/PR16 lidos, demaispendentes iguaisàmain/prefixos;PRsabertos/fechados/commits consultados. MCPoficialread-only/protocolo2025-11-25,schemas/conta/campos/mesmaconversa,sessão,paginação/continuações concluídas;167conciliaçõesPASS,totais1/3/7/14exatos versusGraphGETdiário,aliases selecionados/atribuição unificada.24/novparcialexcluído. Lead=proxycliquepré-navegação,não participante. Baseline36%semdenominador,descritivo. Semrevisãointrarrodada;originais preservados.

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques|LPV|Lead proxy|CVR|CPL|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-23–2026-11-23|experimental|R$146,49|30318|710|571|193|33,80%|R$0,76|
|1|2026-11-23–2026-11-23|controle|R$166,75|24720|678|572|233|40,73%|R$0,72|
|3|2026-11-21–2026-11-23|experimental|R$457,10|90183|2204|1790|681|38,04%|R$0,67|
|3|2026-11-21–2026-11-23|controle|R$466,46|65112|1941|1656|655|39,55%|R$0,71|
|7|2026-11-17–2026-11-23|experimental|R$1027,24|187252|4852|3987|1436|36,02%|R$0,72|
|7|2026-11-17–2026-11-23|controle|R$1046,19|141899|4195|3531|1351|38,26%|R$0,77|
|14|2026-11-10–2026-11-23|experimental|R$2098,12|339429|9813|8018|2859|35,66%|R$0,73|
|14|2026-11-10–2026-11-23|controle|R$2102,05|309086|8611|7258|2749|37,88%|R$0,76|

**Novidades/incerteza:**23/novCVR33,80%/40,73%;7ddiferença-2,24p.p.,IC95%nominal[-4,43;-0,06]. Semanas10–16→17–23/nov: diferençaentremudanças-0,04p.p.,IC95%[-3,10;3,03],entre evoluçõesrelativas0,02pontospercentuais. Campanhasdistintas,eventosatribuídos/dependentes/mix/leiturasrepetidas,não causalidade/resultadoCRO002. Revisões22nov:original+2impressões/controle+1;cloneR$60,98→61,07 e13380→13423impressões,LPV/Leadiguais; snapshotsanteriorespreservados.

**Exposição:**cloneconjunto120252642175430505PAUSED23/nov19:49:04SP;ad120252802517820505PAUSED19:50:03SP,agora1ACTIVE/3PAUSED/2ADSET_PAUSED. Dia23misto,24primeirodiapotencialmentecompletoaindaparcial. Clone23separado242LPV/83Lead/R$50,73/CVR34,30%. Original2ativos/3pausados econtrole1ativo semanticamenteinalterados,orçamentos150/150/50,drafts0. Não atribuirquedaoriginalàpausa doclone/canibalização,sempooling/coortesúnicas. Gestoribombonato deve considerar nova fronteira comfases14/17/19nov;semMetaeditado. PendênciadoID120252802586720505jáencaminhada,nãoinventar identidade/gastooculto.

**Publicação/QA:**main4593aa425ef5f5943d0e0428794ddba957440a03,deployment8014123625success2026-11-23T23:41:38Z/Actions45290913159success,ambosHTMLsHTTP200/byteabyteiguais,coresantigas. Rotaçõeshumanas#67/#69sóURLscontrole,nãoresetambaseline;#71pendentenãoincorporado. Integraçãoprospectivamain+head#16exatamente2coresCSS,controle/scripts/copy/URLsatuaispreservados;20.000/estrelasnão comprovados. FontecandidataidênticaàQAvisual20/nov,semnova captura/implementação/Safari/WebVitalsalegados;NodeVM10casos+igualdadehref/constantePASSemprodução/proposta,semrede/Leadreal/join/mensagem. AutenticaçãoHTTP200/ibombonato/pushconfirmados;sincronizaçãomesmoPR condicionada areadbackremoto.

**Gate/próximo:**ibombonatodecidir#16;apóspublicaçãoPagesSHA+HTML congelar14diasanteriores/excluirdiamixto/revalidaruma vez4170conformeplano. Próximaleitura25nov09hSãoPaulo,dados24novcompleto,primeirodiacivilapóspausasclone,semselecionarendpointoriginal. Materiais/comprovaçãosocialpendentes,semnovacobrança. Execução23novc79f6e8a720e4d7690a751df70699d57completed/Telegramrecibo21329/hashdarespostaextraídaverificados;incidente23outresolved,nãofalhaatual. Schedulerhost/heartbeat/próximarotina25nov12UTCverificados,semreconfiguração. Entregadehojependenteatéconclusão/recibo posterior,semenviopróprio. Artefatosscratch2026-11-24;semmerge/auto-merge/deploy/alteraçãoMeta/controle.


## Acompanhamento diário — 2026-11-25

**Decisão/entrega:** CRO-002 **Em PR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out fechado. [Clone pós-pausa, nova fronteira de orçamento e handoff da entrega](cro/research/2026-11-25-postpause-clone-budget-boundary-and-delivery-handoff.md):24/nov completo conciliado por campanha/conjunto/anúncio/hora; budgets externos25/nov e recibo Telegram24/nov ambíguo diagnosticados. BL-02ICE8/5/8 refinado sem tratamento paralelo. **ibombonato decidir#16** (33dias desdepreparação),não falta amostra/material.

**Fontes:** histórico integralmain/PR16 lido, demaispendentes iguaisàmain/prefixos; PRs abertos/fechados/commits consultados. MCPoficialread-only/protocolo2025-11-25,schemas/conta/campos/mesmasessão/conversa,paginação/continuações concluídas;201conciliaçõesPASS,totais1/3/7/14exatos versusGraphGETdiário. Aliases selecionados/atribuição unificada;25/novparcial excluído. Lead=proxycliquepré-navegação,não participante. Baseline36%semdenominador apenas descritivo.

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques|LPV|Lead proxy|CVR|CPL|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-24–2026-11-24|experimental|R$129,72|21133|537|442|158|35,75%|R$0,82|
|1|2026-11-24–2026-11-24|controle|R$133,63|15959|516|431|178|41,30%|R$0,75|
|3|2026-11-22–2026-11-24|experimental|R$445,69|85828|2042|1658|606|36,55%|R$0,74|
|3|2026-11-22–2026-11-24|controle|R$455,08|62117|1860|1569|629|40,09%|R$0,72|
|7|2026-11-18–2026-11-24|experimental|R$1012,83|186105|4701|3855|1404|36,42%|R$0,72|
|7|2026-11-18–2026-11-24|controle|R$1028,43|137187|4115|3467|1369|39,49%|R$0,75|
|14|2026-11-11–2026-11-24|experimental|R$2084,18|340572|9669|7891|2814|35,66%|R$0,74|
|14|2026-11-11–2026-11-24|controle|R$2097,89|300230|8465|7127|2742|38,47%|R$0,77|

**Novidades/incerteza:**24/novCVR35,75%/41,30%;7ddiferença-3,07p.p.,IC95%nominal[-5,29;-0,84]. Semanas11–17→18–24/nov: diferençaentremudanças-0,49p.p.,IC95%[-3,58;2,61],entre evoluçõesrelativas-1,01pontospercentuais. Campanhasdistintas,eventosatribuídos/dependentes/mix/leiturasrepetidas,não causalidade nemresultadoCRO002. Originais semrevisõeshistóricas;clone23novR$50,73→50,91/impressões10670→10699,LPV/Leadsiguais,snapshots preservados. Consulta MCPsuplementar duplicada deconjuntos24nov sobrescreveu resposta anterior antesdosnapshot; limitação explicitada,não alegar rawintegralmente preservado. Resposta final conciliada; célula iPadcontrole1LPV/2Lead semICbinomial,semtruncamento.

**Exposição:**clone24nov separado207LPV/84Lead/R$44,93/CVR40,58%,somentead120252802517800505 comentrega,primeirodiacivil completo pós-pausas23nov. Hoje25novcontrole150→300às06:43:50SP eclone50→150às06:44:55SP,original150inalterado. Não explicamontem;25misto/26primeirocompletopotencial. Rosteroriginal2ACTIVE/3PAUSED,controle1ACTIVE,clone1ACTIVE/3PAUSED/2ADSET_PAUSED;drafts0. Preservar fases14/17/19/23/25nov,sem pooling/coortesúnicas/canibalizaçãoinferida ouMetaeditado. Gestoribombonato considerar nova fronteira;pendênciaID120252802586720505não resolvida porinferência.

**Publicação/QA:**mainbbd83c30c6e8b33f4ce11f8829fefaeef55ff5a7,deployment8056833291success2026-11-25T12:01:38Z/Actions45609737630success,ambosHTMLsHTTP200/byteabyteiguais,coresantigas. Humanos#71/#74sóURLscontrole/experimental; agente preservouconvitesatuais. Integraçãomain+head#16 exatamente2coresCSS,controle/scripts/copy/URLs preservados;20.000/estrelasnãocomprovados. Capturas390×844/360×800atuaisinspecionadasvisualmente;CTAlegívelinteiro/mesmageometria,semoverflow/cortes/JSexception,foto/seisbenefícios/scroll/focoEnterPASS,extras320/1280PASS. NodeVM10casos+igualdadehref/constantePASSemprodução/proposta,Meta/WhatsAppbloqueadosantesdenavegar,zeroLeadreal/join/mensagem. NãoSafari/WebVitals/lift. Sincronização mesmoPR sujeita areadbackremoto.

![CRO-002 atualizado,não publicado —390×844](cro/screenshots/CRO-002-sync-2026-11-25-390x844.png)

**Operação/gates:**24novexecução8f4a1d1d4c3e40f2bd4984f98e01afb3completed ehashrespostafinalconfere,masponte`partial_ambiguous`/`uncertain`/TimeoutError/message_idnull,semeventosent. Entrega24nov **não confirmada**,não reenviar cegamente;@hermes reconciliarhandle `714c96de5c45/2026-11-24_12-12-29.md` comtransporte autorizado. Falha23outresolved,nãocausaatualdemonstrada. Schedulerativo/heartbeat não confirmaentrega;recibohoje sóapósconclusão,semenviodireto/reconfiguração/outrosperfisalterados.

**Próxima observação:**26nov09hSãoPaulo,dados25novmisto;27novprimeiraleiturapotencial26novcompleto pós-orçamento. ibombonato decidir#16;apóspublicaçãoPagesSHA+HTML congelar14diasanteriores/excluirdiamixto/revalidarumavez4170conformeplano. CRO001não reaberto;nenhumCROnovo/merge/auto-merge/deploy. Materiais/comprovaçãosocial pendentessemrepetição. Artefatos scratch2026-11-25.


## Acompanhamento diário — 2026-11-26

**Decisão/entrega:** CRO-002 **Em PR#16, não publicado**; CRO-001 **Inconclusivo**, endpoint14–21/out fechado. [Dia misto de orçamento, eficiência e guardBL-02](cro/research/2026-11-26-budget-mixed-day-and-test-guard.md):25nov completo reconciliado; aumento devolume não foi confundido com melhoria deCPL/CVR. ICEBL-02 8/5/8 mantido, semtratamento paralelo. **ibombonato decidir#16** (34dias desdepreparação).

**Fontes:** histórico integralmain/PR16 lido, demaispendentes main/prefixos;PRsabertos/fechados/commits conferidos. MCPoficialread-only/protocolo2025-11-25,schemas/conta/campos/mesmasessão/conversa,paginação/continuações concluídas;27checksPASS/12célulasprimáriasMCP×GraphGETdiário exatas,reverificadasindependentemente.26novparcialexcluído. Lead=proxycliquepré-navegação,não participante;baseline36%semdenominador apenasdescritivo.

|Dias|Período São Paulo|Landing|Investimento|Impressões|Cliques|LPV|Lead proxy|CVR|CPL|
|---|---|---|---|---|---|---|---|---|---|
|1|2026-11-25–2026-11-25|experimental|R$152,22|27782|660|525|188|35,81%|R$0,81|
|1|2026-11-25–2026-11-25|controle|R$303,24|42020|1152|960|400|41,67%|R$0,76|
|3|2026-11-23–2026-11-25|experimental|R$428,43|79233|1907|1538|539|35,05%|R$0,79|
|3|2026-11-23–2026-11-25|controle|R$603,62|82699|2346|1963|811|41,31%|R$0,74|
|7|2026-11-19–2026-11-25|experimental|R$1020,98|188957|4680|3819|1400|36,66%|R$0,73|
|7|2026-11-19–2026-11-25|controle|R$1197,59|162129|4699|3959|1595|40,29%|R$0,75|
|14|2026-11-12–2026-11-25|experimental|R$2089,46|347239|9670|7894|2827|35,81%|R$0,74|
|14|2026-11-12–2026-11-25|controle|R$2254,43|317316|9012|7570|2958|39,08%|R$0,76|

**Novidades/incerteza:**25novCVR35,81%/41,67%;7ddiferença-3,63p.p.,IC95%nominal[-5,79;-1,47]. Semanas12–18→19–25nov:diferençaentremudanças-0,90p.p.,IC95%[-3,95;2,15],entre evoluçõesrelativas-2,05pontospercentuais. Campanhasdistintas/eventosatribuídos/dependentes/mix/leiturasrepetidas,nãocausalidade/resultadoCRO002. Original/controlesemrevisõesnosdiascomuns;clone24novR$44,93→45,09,impressões7164→7192,LPV/Leadiguais,snapshotspreservados.

**Exposição/entrega concreta:**25nov misto apósbudgetscontrole150→300às06:43:50SP/clone50→150às06:44:55SP;original150inalterado. Contra médias20–24nov,LPV/dia+87,87%controle/+181,79%clone,mídia/dia+103,68%/+187,09%,masCPL+2,96%/+13,95%. Clone25nov separado656LPV/194Lead/R$139,55/CVR29,57%;sem pooling/canibalizaçãoinferida. BL-02agoraexplicita casodeaceitaçãocontra tratar25misto como26completo ouescolher24isolado;primáriaoriginal/CVR/planoCRO002inalterados. Roster/configuração semanticamenteigualàontem,drafts0,miniaturaassinada separada;fases14/17/19/23/25preservadas.

**Publicação/QA:**mainbbd83c30c6e8b33f4ce11f8829fefaeef55ff5a7/deployment8056833291success2026-11-25T12:01:38Z/Actions45609737630success,ambosHTMLsHTTP200byteabyteiguais,coresantigas. PR75/73operacionaispendentesapenasURLs,nãoincorporados. Integraçãomain+head#16exatamente2coresCSS;controle/copy/scripts/URLsatuaispreservados;20.000/estrelasnãocomprovados. FonteidênticaàQAvisual25nov390×844/360×800,hashesconferidos,semnova captura/implementação/Safari/WebVitalsalegados. NodeVM10casos+igualdadehref/constantePASS,semrede/Leadreal/join/mensagem. AtualizaçãomesmoPR/readbackremotoobrigatório.

**Operação/próximo:**25novexecuçãof7b2024c8fa34f269af378320a9fc598completed/Telegramrecibo21669às12:20:45Z/hashdarespostafinalextraídaconferido;24novcontinuaambíguo,@hermesreconciliarsemreenviocego. Incidente23outresolved,nãofalhaatual. Agendaefetivalida **01hSãoPaulo/04hUTC**,não09hdocontextoantigo;nenhumaalteraçãoagendadaexecutada. Próximarotina27nov01hSPinclui26novcompleto,primeirodiacivilpós-orçamento,comatençãoabackfill. Entregahoje sóapósconclusão/recibo posterior,semenviopróprio. ibombonatodecidir#16;apóspublicaçãoPagesSHA+HTMLcongelar14diasanteriores/excluirdiamixto/revalidaruma vez4170conformeplano. Materiaispendentessemcobrançarepetida;semCROnovo/Metaeditado/merge/auto-merge/deploy. Artefatos scratch2026-11-26.


## Acompanhamento diário — 2026-11-27

**Decisão/entrega concreta:** CRO-002 **Em PR#16, não publicado**; CRO-001 permanece **Inconclusivo**, endpoint14–21/out encerrado. [Diagnóstico verificável do gate de aprovação e primeiro dia inteiro pós-orçamento](cro/research/2026-11-27-approval-gate-and-complete-budget-day.md). Simulação de integração#16 sem conflito/exatamente duas cores; zero checks/status contexts/Actions no head e zero reviews. `pending` sem contexts não é CI falhando. **ibombonato: decidir aprovar, ajustar ou rejeitar#16**; não falta volumeCRO001/material. ICE da hipótese operacional7/9/8, semIDCRO novo nem tratamento simultâneo. PR31 conflita;#40/#41 são outras rotas e integram sem conflito por retorno ao merge-base — aviso para decisão separada do responsável, sem editar/fechar essesPRs.

**Fontes:** histórico integralmain e PRs pendentes, PRs abertos/fechados e publicação conferidos. MCP oficial read-only/schema/conta/campos/sessão/protocolo2025-11-25; GraphGET diário e atividades paginadas. **12/12células primárias exatas**,526arquivos do manifesto conferidos pelo pai; **24/30checks gerais**,6marginais divergentes preservados e detalhados na pesquisa. Não declararPASSglobal nem usar marginais incoerentes para explicar mix. 27nov parcial excluído; Leadproxy=clique pré-navegação,não membro. Baseline36%semdenominador descritivo.

|Dias|Período São Paulo|Landing|Mídia R$|Impressões|Cliques|LPV|Lead proxy|CVR|CPL R$|
|---|---|---|---:|---:|---:|---:|---:|---:|---:|
|1|2026-11-26–2026-11-26|experimental|130,28|21916|552|415|138|33,25%|0,94|
|1|2026-11-26–2026-11-26|controle|245,99|31136|843|712|262|36,80%|0,94|
|3|2026-11-24–2026-11-26|experimental|412,24|70835|1749|1385|486|35,09%|0,85|
|3|2026-11-24–2026-11-26|controle|682,94|89124|2512|2103|840|39,94%|0,81|
|7|2026-11-20–2026-11-26|experimental|997,18|181859|4505|3649|1328|36,39%|0,75|
|7|2026-11-20–2026-11-26|controle|1293,72|172412|5012|4227|1673|39,58%|0,77|
|14|2026-11-13–2026-11-26|experimental|2076,19|348907|9539|7760|2793|35,99%|0,74|
|14|2026-11-13–2026-11-26|controle|2353,19|325306|9228|7754|3022|38,97%|0,78|

**Novidade desdeontem:**26nov é primeiro dia civil completo pós-aumentos externos25nov06:43:50SPcontrole150→300 e06:44:55SPclone50→150;original150inalterado. Contra25nov reconsultado,CVRoriginal35,98→33,25%/controle41,67→36,80%;CPL+17,82%/+23,82%. Clone separado472LPV/117Lead/CVR24,79%/CPLR$1,07. Versus20–24nov,controle511→712LPV/dia eR$148,882→245,99mídia/dia;um dia não demonstra efeito orçamento/landing/canibalização. Gap7doriginal−controle−3,19p.p.[−5,33;−1,04];semanas13–19→20–26novdiferençaentremudanças−0,57p.p.[−3,63;+2,48],entreevoluçõesrelativas−1,35pontospercentuais. Descritivo,nãocausal/nãoresultadoCRO002. Backfill26novcontrole705/260→712/262eclonemarginais preservados;25novoriginal525/188→528/190,demaisrevisõesna pesquisa.

**Exposição/QA:**semnovaedição semântica Meta porID;drafts0;132atividadesGraph/2páginasexauridas,zeroeventosnovos versus26nov;URLsassinadas históricas não sãoedições. PublicaçãoSHA79133f0fdddbfc64cd1c84ac0465c41a27eadf70/deployment8100580176success2026-11-27T02:54:01Z/Actions45930958360success;ambosHTMLsHTTP200byteabyteiguaisàmain,coresantigas. #76/#77publicados apenasURLscontrole/index.html;#75fechadosemmerge. Propostaintegraexatamentemain+duascores,controle/URLs/scripts/copyhumana preservados;20.000/estrelasnãocomprovados. Fonteindex3igualàQAvisual25nov390×844/360×800,hashesconferidos;nenhumanovacaptura/implementaçãoalegada. NodeVM10casos+href/constantePASS,zeroLeadreal/join/mensagem.

**Operação/próximo:**26novexecuçãob1bcf2f6282144b4bf706275ad7c453ecompleted/Telegramrecibo21722às04:15:46Z/hashfinalconferido. Incidente23outresolved;24novambíguonãoreenviado. Próximarotina28nov **01hSP/04hUTC**,horárioefetivoverificado,diferentedopromptantigo09h,semalterarscheduler. Recibodehojependentedaconclusão;semenviopróprio. Reconsultar6marginais/backfill26nov e27novcompleto;ibombonatodecidir#16. Apóspublicação confirmadaPagesSHA+HTML,congelar14diasanteriores/excluirdiamixto/revalidaruma vezreferência4170conformeplano. Materiais/provasocialpendentessemcobrançarepetida. NenhumaalteraçãoMeta/controle/merge/auto-merge/deploy. Artefatos scratchcro-icb-2026-11-27.
