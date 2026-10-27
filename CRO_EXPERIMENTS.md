# Histórico de experimentos CRO — ICB

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
