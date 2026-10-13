# Histórico de experimentos CRO — ICB

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

## Experimentos

Nenhum experimento novo implementado nesta execução. Não atribuir IDs retrospectivos ou resultados inventados a PRs antigos. O próximo experimento novo deve usar **CRO-001** após consulta deste histórico e dos PRs.

Cada registro deve conter ID sequencial; criação e publicação real; status (Proposto, Em PR, Em avaliação, Vencedor, Perdedor ou Inconclusivo); problema/hipótese/evidências; mudança objetiva; métricas antes e depois para ambas as campanhas; períodos exatos; impacto absoluto e relativo; incertezas, conclusão e aprendizados; PR, commit de publicação e screenshot mobile 390×844. Atualizar sem apagar registros anteriores. Dados posteriores ficam pendentes até a publicação confirmada; nenhum experimento é vencedor só porque subiu num dia.

## Diagnóstico de 2026-10-13

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

## Hipóteses em backlog — nenhuma implementada

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

## Próxima execução

1. Ler este arquivo completo na versão mais recente de `main` **e nas branches/PRs de CRO pendentes**. Se o PR de histórico não tiver sido integrado, reutilizar/atualizar esse PR; não criar inicialização duplicada.
2. Confirmar nova publicação e destinos sem os alterar. Separar dados anteriores/posteriores à publicação de 2026-10-13T19:50:46Z; métricas diárias não isolam a hora de publicação. A primeira data inteiramente posterior é 2026-10-14 no fuso da conta; acumular volume e consistência, não impor um número fixo de dias como aprovação.
3. Reconsultar janelas completas e eventuais revisões de atribuição. Só abrir um PR de experimento quando não houver outro pendente e houver referência adequada, registrando CRO-001 com métricas exatas e gates mobile.
4. Obter comprovação verificável do número/prova social antes de qualquer novo uso. Se ela não existir, propor tratamento verdadeiro em mudança separada, sem inventar substitutos.
5. Não atribuir os resultados desta coleta ao histórico novo: documentação não alterou o funil. Nenhum vencedor/perdedor foi declarado.

**PR de acompanhamento (documentação, não experimento):** [#15 — iniciar histórico e diagnóstico ICB](https://github.com/ibombonato/promos-da-lidi/pull/15), aberto para aprovação humana; sem merge ou publicação nesta execução.
