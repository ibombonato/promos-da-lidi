# Histórico de experimentos CRO — ICB

> **Atualização de 2026-10-13 após merge humano:** **CRO-001 está Em avaliação**, com publicação confirmada no commit `1a377ea858b18189d7b40b1fd63990376e777712`; o build Pages terminou em 2026-10-13T23:42:37Z (20:42:37 em São Paulo) e o HTML público conferiu byte a byte. A rotina diária está agendada às 09h de São Paulo. Rotações operacionais de convite não reiniciam a avaliação de Lead/LPV. Os registros iniciais foram preservados como histórico, não como orientação vigente.

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

**Status:** Em avaliação

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

**Período atual:** 2026-10-14 a 2026-10-17, quatro dias completos após a publicação do CRO-001; snapshot consultado em 2026-10-18. O dia 2026-10-13 contém tratamentos misturados e fica excluído da comparação diária principal. Snapshots anteriores permanecem nas seções datadas; pendente não significava zero. **Novo fator externo:** orçamento experimental mudou de R$100/dia para R$150/dia em 17/out às23:40:22 de São Paulo. O headline não mudou; manter acumulado e baseline, sinalizar17/out como dia de orçamento misto e acompanhar separadamente14–16/out e os dias completos desde18/out.

| Métrica | Experimental | Controle |
|---|---|---|
| Landing Page Views | 1693 | 3886 |
| Leads atribuídos (proxy clique) | 697 | 1527 |
| CVR | 41,17% | 39,29% |
| Investimento | R$ 384,70 | R$ 765,44 |
| CPL proxy | R$ 0,55 | R$ 0,50 |

**Variação observada pós−pré em p.p.:** Experimental +4,19; controle +1,48. IC95% nominal aproximado experimental +1,52 a +6,87 p.p., sem ajuste para leituras sequenciais. Diferença entre mudanças absolutas +2,71 p.p., IC95% aproximado −0,56 a +5,98 p.p. Não é impacto causal comprovado.

**Variação relativa observada em %:** Experimental +11,34%; controle +3,92%. Diferença entre evoluções relativas +7,42 pontos percentuais de variação relativa, descritiva.

**Conclusão atualizada em 2026-10-18:** Manter Em avaliação; resultado ainda inconclusivo. Apenas1693LPV (41,01% da referência4128), cobertura quarta–sábado, controle também melhorou, diferença entre mudanças incerta e shareLPV do principal anúncio81,77%pré→90,55%pós. Não parar por intervalo nominal favorável. Aumento externo de orçamento confirmado por Graph GET; MCP de atividades retornou vazio e não prova ausência de edição. Sensibilidade14–16/out, inteiramente anterior à edição de orçamento:519/1258=41,26% vs1146/2915=39,31%, diferença entre mudanças+2,78p.p.,IC95%−0,88 a+6,44; também inconclusiva. Não reiniciar baseline nem lançar outro tratamento; avaliar mix/atribuição na nova fase de entrega. Rotações de convite continuam operacionais. O agente não alterou Meta nem landings.

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
