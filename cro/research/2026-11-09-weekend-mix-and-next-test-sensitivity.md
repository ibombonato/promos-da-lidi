# BL-02 — sensibilidade por anúncio e dispositivo em fins de semana comparáveis

**Data:** 2026-11-09. Diagnóstico/pesquisa somente leitura; não implementação, CRO-003 ou reabertura do CRO-001. CRO-002 permanece Em PR #16, não publicado.

## Evidência nova: a recuperação de domingo não elimina a queda recente

MCP oficial e série diária Graph atuais conciliados nas janelas1/3/7/14dias. Como investigação exploratória adicional, Graph GET ad-day e device-day de31/out–08/nov foram reconsultados nesta execução. Contagens por campanha/data conciliam exatamente com a série atual; resíduos monetários de breakdown inferiores a um centavo preservados. Aliases Lead/LPV selecionados, nunca somados. Nenhuma configuração Meta modificada.

| Fim de semana completo, São Paulo | Experimental: Leads/LPV, CVR | Controle: Leads/LPV, CVR |
|---|---|---|
| 31/out–01/nov |546/1360,40,15%|530/1361,38,94%|
| 07–08/nov |474/1367,34,67%|479/1284,37,31%|

A experimental varia **−5,47p.p.**, IC95% nominal aproximado−9,10a−1,85; controle−1,64p.p., IC95%−5,34a+2,07. Dias da semana são iguais, mas visitantes/mix/leilões não são randomizados nem pareados. A edição externa16.000→20.000 em02/nov ocorreu entre os períodos; não se pode isolar seu efeito, da landing ou dos criativos. Este recorte é diagnóstico escolhido hoje, **não endpoint de experimento nem nova regra de baseline**. Não apresentar seu intervalo como prova causal ou parada por significância.

## Decomposição por anúncio: maior share dos novos não explica toda a variação

Identidade simétrica: composição = soma[(w1−w0)×(p0+p1)/2]; dentro = soma[(p1−p0)×(w0+w1)/2]. Cálculo antes de arredondar, soma validada contra a mudança agregada.

- Fins de semana: **−5,47p.p. = −0,29 de composição −5,18 dentro dos anúncios**. Padronizar taxas posteriores aos pesos deLPV anteriores produz34,56%, perto dos34,67% observados; não remove a queda.
- Os dois anúncios lançados21/out passam de783/1360LPV para1085/1367LPV; suas taxas agrupadas passam302/783=38,57%→379/1085=34,93%. Não tratá-los como uma alocação50/50 ou candidatos comprovadamente inferiores.
- Recuperação07→08/nov: **+4,69p.p. = +0,07 de composição +4,63 dentro dos anúncios**. Novos224/595=37,65% no domingo, contra155/490=31,63% no sábado. Essa melhora é observacional, não efeito do contraste ainda não publicado.

“Dentro” engloba variação de audiência, intenção, dia, atribuição e demais fatores; **não equivale a efeito de copy, criativo ou landing**. Todos os quatro anúncios têmLPV em ambos os recortes; não houve imputação de célula ausente. IDs/estados/configuração atuais foram comparados pela união deIDs; somente miniatura assinada do antigo anúncio pausado varia frente à véspera.

## Dispositivo: não há base para culpar Safari

Análise marginal separada, explicitamente restrita aAndroid smartphone+iPhone. Cobertura experimental1359/1360→1366/1367LPV, todos546→474Leads; controle1360/1361→1282/1284LPV, todos530→479Leads. Outros dispositivos permanecem nos raws/totais principais; não foram declarados zeros observados.

| Smartphone experimental | Antes, Leads/LPV, CVR | Depois, Leads/LPV, CVR |
|---|---|---|
| Android |406/926,43,84%|316/873,36,20%|
| iPhone |140/433,32,33%|158/493,32,05%|

A queda smartphone experimental−5,48p.p. decompõe−0,33 de composição e−5,15 dentro; a taxa iPhone ficou quase igual entre os fins de semana, enquantoAndroid caiu. Não inferir bug deSafari nem causaAndroid. Decomposições marginais por anúncio/dispositivo **não podem ser somadas** ou interpretadas como ajuste conjunto. Falha inicial do guard detectou dispositivo `other` ausente no segundo período; a sensibilidade foi explicitamente delimitada aos dois smartphones, com cobertura e reconciliação integral preservadas, em vez de inventar CVR de uma célula vazia.

## Refinamento concreto do próximo teste BL-02

**Problema/alteração objetiva mantidos:** módulo hero mobile ocupa248px antes da oferta; após avaliar/encerrarCRO-002, testar somente sua compactação por largura, comfoto88px/hero136px já prototipados offline. Headline, argumentos, CTA, tracking e rotas permanecem iguais àversão imediatamente anterior. Ganho geométrico129px já medido em pesquisa; compreensão/confiança/CVR ainda não medidas. ICE **I8/C5/E8** mantido, sem elevar confiança pelo diagnóstico observacional.

**Acréscimo ao plano, sem gate arbitrário:** congelar pesos por anúncio e por smartphone da janela pré-publicação, guardar cobertura de IDs/células e apresentar separadamente primária agregada, padronização por anúncio e sensibilidade smartphone. Se uma célula não tiverLPV, registrar taxa não estimável e cobertura, sem imputa-la; adições/remoções recebem diagnóstico separado. Conferir dias da semana no checkpoint planejado, não escolher um fim de semana favorável como novo desfecho. Não somar decomposições marginais. Esse protocolo reduz o risco de chamar mudança de distribuição de lift da primeira dobra; não transforma o teste observacional emA/B randomizado. Dimensionamento e baseline próprios só quando elegível, antes de observar resultados.

BL-01 exige materiais reais já solicitados; sem resposta registrada. BL-02 continuafallback sem esses materiais; BL-03 mantém custo deatenção de91px documentado ontem, abaixoBL-02; BL-06 mantém riscos de clareza de canal/grupo. Nenhuma exposição alterada ou IDnovo atribuído. Prova social20.000/estrelas continua sem comprovação; pedido complementado03/nov permanece pendente, sem nova cobrança diária.

## Gate e responsável

GitHubGET `/user` com credencial salva voltouHTTP401Badcredentials; não presumir causa, não tentar escrita. **ibombonato/@hermes:** restaurar autenticação segura, confirmar identidade/permissão e sincronizar o mesmoPR#16 com main/convites/conteúdo atuais e todo histórico antes da decisão humana. Branch remota ainda headf9286a3, semmerge/auto-merge/comentários/reviews novos. Não aprovar como se sincronizada; não criar experimento paralelo. Registros01–09/nov ficam locais emcommit/patch até desbloqueio.

Publicação atual confirmada separadamente: Pagesdeployment7630609976success/Actions42441187719success paraSHA3c93fbe7d7263d6b47cdfa2f0523f8e1c79602cc, HTMLs públicos de ambas landings byte a byte iguais. Verde antigo publicado; não há métrica posteriorCRO-002. Após eventual aprovação, confirmar novoSHA+HTML, congelar14dias completos anteriores, excluir dia misto e revalidar uma vez a referência4170 conforme plano original. Não falta volumeCRO-001 ou material para contraste.

**Artefatos:** `~/work/hermes-scratch/cro-icb-2026-11-09/`: `weekend-current-raw.json`, `weekend-diagnostic.json`, `weekend_diagnostic.py`, rawsMCP/Graph atuais, `today-validation.json`, validaçõesCTA e recibo anterior verificado. SemHTML/CSSnovo: nenhuma novaQAvisual mobile alegada; guard de escopo eNodeVM doCTAreal passaram semrede/eventosMeta/join. Nenhum merge/deploy ou alteração Meta/controle/rotas/rastreamento.
