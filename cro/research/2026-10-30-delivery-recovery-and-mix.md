# Retomada de entrega e composição de tráfego — 30/out/2026

## Entrega concreta e decisão

**Primeiro dia completo com retomada de entrega experimental confirmado: 29/out.** Atualiza o [incidente diagnosticado em29/out](2026-10-29-experimental-delivery-collapse.md), sem apagar a queda de28/out ou declarar sua causa resolvida. MCP oficial e Graph GET confirmam entrega próxima de27/out; não se trata mais somente da retomada parcial observada ontem de manhã. Não há evidência de recuperação sustentada em vários dias ou de ganho de conversão da landing.

**CRO-002 continua Em PR #16, não publicado.** O gate é decisão humana de ibombonato, seguida de confirmação Pages SHA+HTML; nenhum teste adicional/alteração de HTML foi iniciado. Não aguardar mais volume deCRO-001, encerrado Inconclusivo. A retomada não exige reset de baseline, exclusão retrospectiva de28/out nem mudança do checkpoint já registrado.

## Evidência atual, read-only

Dias completos em America/Sao_Paulo; valores reconsultados hoje, não preenchidos com snapshots anteriores.

| Experimental | 27/out, antes da queda | 28/out, incidente | 29/out, retomada completa |
|---|---:|---:|---:|
| Investimento | R$172,39 | R$2,80 | R$171,99 |
| Impressões | 40042 | 591 | 37328 |
| Cliques no link | 873 | 16 | 836 |
| LPV | 740 | 16 | 711 |
| Leads proxy | 268 | 4 | 276 |
| CVR | 36,22% | 25,00% | 38,82% |

29/out versus27/out: investimento−0,23%, impressões−6,78%, cliques−4,24%, LPV−3,92%, Leads+2,99%. Comparação de dias distintos, não equivalência estatística nem efeito causal. CVR de29/out: Wilson95%35,31–42,45%; diferença contra controle+2,26p.p., IC95%aproximado−2,86a+7,39. Não declarar vencedor.

Graph GET separado de entrega e breakdown horário reconciliam exatamente R$171,99/37328impressões/836cliques com MCP e série diária. Há entrega reportada em00h e de06h a23h; não uma única explosão à meia-noite. A série horária é atribuída ao fuso do anunciante. Controle29/out: R$140,00/33090impressões/764cliques, igualmente conciliado. Consulta de30/out em torno09hSãoPaulo: experimental R$34,68/6452impressões/152cliques; parcial, não projeção para o restante do dia nem segundo dia completo recuperado.

Conta ativa, disable_reason0, spend_cap0; campanha/conjunto e quatro anúncios experimentais ACTIVE, antigo PAUSED. Controle ACTIVE; ambos orçamentos nominaisR$150/dia. MCPerrors[] e ferramenta de anomalia sem sinal; 39atividadesGraph examinadas, paginação esgotada, nenhuma nova edição relevante desde a redução externa do controle27/out. Ativos/conjuntos/copy completa/destinos/UTMs/tracking/atribuição iguais àconsulta anterior; somente miniatura assinada do antigoPAUSED mudou. **Esses dados não identificam a causa da interrupção nem descartam pacing, billing ou restrições não expostas.**

## Mix mudou de forma relevante na retomada

Ad-day27–29/out reconsultado hoje; todas as contagens e investimento conciliam exatamente com cada total campanha/dia. Lead é clique pré-navegação, não confirmação de entrada ou qualidade do participante.

| Anúncio experimental | LPV/Leads27/out | LPV/Leads29/out | Investimento29/out |
|---|---:|---:|---:|
| `120250848857170505`, texto4em1 | 36/17 | 35/11 | R$7,44 |
| `120251541120490505`, produtos atualizados | 518/186 | 358/141 | R$89,07 |
| `120252297350870505`, novo | 155/57 | 299/119 | R$71,35 |
| `120252297350880505`, novo | 31/8 | 19/5 | R$4,13 |

Os dois anúncios novos passaram de25,14% dos LPV em27/out para **44,73% em29/out**, 318LPV/124Leads/R$75,48. Não repetir a participação residual observada em22/out nem concluir teste50/50 ou superioridade dos criativos. Decomposição simétrica da mudança agregada27→29/out **+2,60p.p. = +0,31p.p. composição +2,29p.p. dentro dos anúncios**, identidade reconciliada sem arredondar parcelas previamente. “Dentro” não isola causa: horário, público/dispositivo e outras condições também podem mudar dentro de cada anúncio. Não atribuir toda a recuperação da taxa ao novo mix ou a uma landing que não mudou.

**Aprendizado aplicável ao backlogBL-02:** manter primária agregada e sensibilidade por anúncio/IDs/pesos congelados no pré da futura publicação, conforme plano já preparado; registrar cobertura de cada estrato. Não congelar pesos de um único dia recuperado nem excluir silenciosamente dias de subentrega. Nenhum novo ID CRO, threshold ou calendário de teste foi criado.

## Encaminhamento e próxima observação

- **ibombonato/gestor autorizado:** registrar no Ads Manager o motivo da interrupção de28/out e eventual aviso/limite/cobrança daquele período. A entrega voltou no primeiro dia completo seguinte; não recomendar pausa/escala “corretiva” sem causa verificada. Se reaparecer forte subentrega, encaminhar ao suporteMeta os IDs, dias e conciliação deste documento e do diagnóstico anterior. Este registro não é um chamado externo aberto nem pressupõe resposta do gestor.
- **ibombonato:** decidir o [PR#16](https://github.com/ibombonato/promos-da-lidi/pull/16), contraste isolado, mantendo a ressalva já registrada de href sem query versus constante parametrizada. Não há resposta nova noPR; nenhuma uniformização de destino/parâmetro autorizada. O PRoperacional#24 antigo continua separado, não mesclado/fechado pelo agente.
- **Próxima rotina existente,31/out09hSãoPaulo:** incluir30/out completo, checar persistência da entrega/mix e decisão/publicação. Isso é observação de estabilidade do incidente, não uma nova janela obrigatória para preparar/publicar contraste. Se publicado, congelar os14dias anteriores conforme regra e excluir dia misto; preservar a subentrega nas métricas e explicitá-la nas sensibilidades. Referência original4170LPV só terá a revalidação única prevista no congelamento, não um novo alvo diário.
- Pedido de ofertas reais/print autorizado e comprovação de16.000/estrelas feito em23/out continua pendente, sem repetição de cobrança; não bloqueia o contraste.

## Artefatos, QA e limites

Dados atuais em `~/work/hermes-scratch/cro-icb-2026-10-30/`: respostasMCP1/3/7/14dias, daily-graph.json, analysis.json, traffic-audit.json, activities.json, delivery-probe.json, mcp-delivery-diagnostics.json, ad-daily-recovery-raw.json, recovery-mix.json e today-validation.json. Reutilização de código anterior, nunca substituição de dados atuais.

Guard de escopo PASS: index3 difere da main somente em duascoresCSS; controle/scripts/links/copy preservados. NodeVM sem rede:10casos comportamentaisPASS emprodução/proposta; igualdade literalhref/constanteFAIL preservada e encaminhada, sem normalizarquery ou alegar rota quebrada. Nenhum eventoMeta real/entradaWhatsApp. Sem nova implementação visual: screenshots390×844/360×800 doCRO-002 continuam os originais; não alegar nova QAvisual, Safari ou mediçãoWebVitals.

Pages/main `c8a16941814a43a040506a5330903587e5c16852`, built26/out02:08:45Z; HTML público das duas páginas conferiu byte a byte com essecommit, cores antigas emprodução. Baseline histórico36% sem denominador é descritivo. Campanhas distintas/eventos atribuídos e dependentes limitam causalidade e os intervalos binomiais aproximados.
