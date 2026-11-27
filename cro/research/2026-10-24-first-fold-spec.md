# BL-02 — Especificação da primeira dobra compacta

**Preparada em:** 24/10/2026. **Estado:** backlog especificado, não implementado; não é CRO-003. O CRO-002 continua sendo o único experimento em PR (#16). Este documento não altera o tratamento, o plano de avaliação ou as cores propostas naquele PR.

## Evidência específica acrescentada hoje

Auditoria da **produção**, não de um novo tratamento: Chromium real a390×844 e360×800; screenshots inspecionados. Rede Meta/WhatsApp bloqueada antes de navegar; nenhum clique no CTA. HTML público conferido com main48a3628; o CTA publicado ainda tem o gradiente anterior aoCRO-002.

| Elemento | 390×844 | 360×800 |
|---|---:|---:|
| Hero de marca | 248px de altura | 248px de altura |
| Foto | 128×128px, termina emy284 | 128×128px, termina emy284 |
| Início da headline | y299 | y299 |
| CTA | y503,75–565,75 | y500,14–560,14 |
| Grade de benefícios | y732,13–1041,88 | y726,52–1049,70 |
| Altura total do documento | 1068px | 1076px |

**Inspeção visual:** marca e foto precedem a proposta; oferta e botão são legíveis e inteiros. Em390 a primeira linha de benefícios aparece; em360 aparecem os ícones e só parte da primeira linha. Sem corte horizontal, sobreposição ou exceçãoJS observada. Não é testeSafari ou WebVitals de campo. A posição do CTA **já é visível**: não há diagnóstico de botão escondido. A auditoria não comprova que o espaço inicial cause abandono, nem valida a alegação16.000/estrelas existente.

Evidência de fonte: `index3.html`, media query móvel, `.hero` min-height248px/padding24px20px76px; `.profile`128px/bottom−36px; `.content`padding-top51px. A altura inicial não decorre de formulário ou funcionalidade indispensável. A pesquisa de23/out continua como contexto, não prova deCVR concorrente.

## Problema, hipótese e tratamento delimitado

**Problema hipotético:** visitante frio precisa atravessar um cabeçalho dominado pela marca antes de ler a oferta. Parte dos benefícios fica abaixo da dobra, apesar de a ação já estar disponível.

**Hipótese:** um cabeçalho móvel compacto, mantendo identidade pessoal, mesma promessa, argumentos e ação, permitirá entender oferta e benefícios com menos varredura visual e poderá aumentarLead/LPV. Avaliar o **módulo de hierarquia** como intervenção única; não alegar isolamento individual de foto, altura e margem.

**Especificação candidata para quando elegível, ainda sem renderização/QA do tratamento:**

- Somente no breakpoint móvel já existente; preservar o desktop.
- Hero com alvo136px e padding16px20px32px, em vez de248px; marca em34px e assinatura26px, ainda reconhecíveis; adequar a curva e ornamentos decorativos a essa caixa sem sobrepor texto/foto.
- Foto atual preservada, sem novo asset:88×88px, bottom−24px. Não remover autoria nem mudar imagem/alt.
- Padding superior de`.content`34px, mantendo22px laterais e26px inferior.
- Headline doCRO-001 e o parágrafo de curadoria literalmente preservados. CTA inteiro, aria-label, geometria, cores da versão efetivamente aprovada, foco, hover, href/constante, Pixel/scripts/delay150ms e restantes seções inalterados.
- Sem novos textos, urgência, descontos, prova social, exemplos,FAQ, barra fixa ou segundo botão. Não alterar convites nem incorporar a rotação pendente#23 por iniciativa própria.

**Estimativa geométrica, não resultado renderizado:** redução pretendida112px nohero e17px no padding-content deslocaria o fluxo em129px, se nenhuma quebra de linha/altura intrínseca interferir. O topo doCTA ficaria perto de375px em390 e371px em360. Validar isso quando prototipar; não forçar a meta comprimindo fontes da oferta ou o botão. Se a marca/foto ficarem ilegíveis ou o hero crescer por conteúdo, rever o protótipo antes de abrir experimento.

**ICE qualitativo:** Impact8/Confidence5/Ease8. Evidência forte do espaço ocupado, confiança apenas moderada na hipótese comportamental; nenhum ganho previsto. BL-01 continua primeira oportunidade se os exemplos reais forem fornecidos. BL-02 é fallback sem dependência de material, não motivo para abandonar ou ultrapassarCRO-002.

## Critérios verificáveis da futura implementação

1. Elegibilidade: CRO-002 explicitamente avaliado/encerrado, sem outroPR experimental pendente. Reconsultar main, convites atuais, PRs e publicação. SeBL-01 já tiver materiais próprios autorizados, reavaliar prioridade antes de implementarBL-02.
2. Guard de escopo: CSS do módulo inicial mobile é a única diferença; todo o corpoHTML e scripts/URLs iguais ao baseline então vigente. Controle idêntico. Comparar byte a byte, não apenas screenshot.
3. Chromium390×844/360×800: marca inteira, foto reconhecível, headline/copy sem redução de legibilidade, sem colisões/overflow; CTA mantido com pelo menos a dimensão atual; mais conteúdo útil acima da dobra sem retirar a Lidi. Também320px e desktop, scroll, foco/Enter e reduced-motion.
4. NodeVM do script real sem rede: Lead antes do timer/redirecionamento normal, trackingausente/erro, delay150ms, modificadores/botões/eventocancelado, fallbackhref coerente. Não emitir eventos reais nem abrirWhatsApp.
5. Fotografar e inspecionar o **tratamento real** quando implementado, incluindo antes/depois; estas capturas de24/out são exclusivamente baseline. PR futuro com histórico e screenshots, sem merge/deploy.

## Plano de avaliação proposto — não substitui o doCRO-002

- Leadatribuído/LPV principal, CPLproxy secundário. Não medir sucesso porCTA mais alto nem por maior número de benefícios visíveis.
- Pré-período somente da versão imediatamente anterior, regra proposta:7dias completos antes da publicação, ampliando **para trás dentro do mesmo tratamento** se necessário para volume/cobertura. Se faltar baseline utilizável, declarar exatamente essa limitação; não preencher com dias de outra versão.
- ConfirmarPagesSHA+HTML e excluir o dia parcialmente exposto; uma avaliação principal no checkpoint de volume com cobertura dos dias da semana, sem parada por primeiroIC favorável.
- MDE de planejamento proposto+3p.p., alfa5% bilateral/poder80%; recalcular amostra e projeção ao congelar baseline, antes de olhar o pós. Não usar4170doCRO-002 como limiar universal e não prometer data de vitória.
- CVR/CPL ponderados, IC95% aproximados, evolução do controle e sensibilidades por anúncios, orçamento, dispositivo/posicionamento e dias da semana; não randomizados e não coortes deduplicadas. Se evidência insuficiente no checkpoint, encerrarInconclusivo, sem prolongar só para significância.

**Material:** nenhum adicional paraBL-02. Pedido de três ofertas reais eprintanonimizado de23/out permanece pendente paraBL-01, sem nova cobrança hoje. Comprovação de16.000/estrelas continua pendente; não usar a existência noHTML como validação ou ampliar a alegação. Sua eventual correção é uma intervenção separada, não embutida no módulo.

**Artefatos da auditoria:** `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-24/`: `baseline-mobile-audit.json`, `baseline-390x844.png`, `baseline-360x800.png` e `live-validation.json`. Nenhum protótipo doBL-02 foi colocado noHTML/produção/PR.
