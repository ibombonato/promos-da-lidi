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

**Período:** A partir de 2026-10-14, primeiro dia completo após a publicação do CRO-001. O dia 2026-10-13 contém tratamentos misturados e fica excluído da comparação diária principal. Na confirmação de publicação ainda não existe dia posterior completo; métricas abaixo permanecem pendentes, não zero.

| Métrica | Experimental | Controle |
|---|---|---|
| Landing Page Views | Pendente | Pendente |
| Leads atribuídos (proxy clique) | Pendente | Pendente |
| CVR | Pendente | Pendente |
| CPL proxy | Pendente | Pendente |

**Impacto absoluto em p.p.:** Pendente.

**Impacto relativo em %:** Pendente.

**Conclusão:** Publicação confirmada após merge humano; experimento em avaliação. Ainda não existe dia posterior completo nem evidência de impacto. Não declarar vencedor/perdedor agora.

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
