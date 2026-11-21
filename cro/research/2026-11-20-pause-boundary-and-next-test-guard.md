# Fronteira das pausas e preparação da próxima avaliação — 20/nov/2026

Pesquisa/diagnóstico documental, não CRO-003 nem alteração da exposição. CRO-002 continua Em PR #16 e não publicado; CRO-001 permanece encerrado Inconclusivo no endpoint14–21/out.

## Evidência nova, conciliada

MCP oficial somente leitura, Graph GET diário/ad-day/horário e hierarquia atuais, cutoff19/nov completo em America/Sao_Paulo. 140 verificações aprovadas; cinco grandezas principais exatas em1/3/7/14dias, contagens de breakdown exatas, maior resíduo monetário R$0,000001. Raws e `pause-boundary-19nov.json` em `~/work/hermes-scratch/cro-icb-2026-11-20/`. Não usar dados antigos como atuais.

| Experimental | 18/nov | 19/nov |
|---|---:|---:|
| Todos os anúncios, Leads/LPV | 192/561 | 212/588 |
| CVR | 34,22% | 36,05% |
| Somente os mesmos dois IDs sobreviventes, Leads/LPV | 176/502 | 212/588 |
| CVR desses dois IDs | 35,06% | 36,05% |
| Par pausado: gasto / impressões / LPV / Leads | R$16,55 / 2948 / 59 / 16 | R$0,03 / 5 / 0 / 0 |

Pausas externas finais dos anúncios `120250848857170505` e `120252297350880505`:19/nov00:08:34 e00:08:37SP. **19/nov contém8min37s anteriores à última pausa, não24h estritamente posteriores.** Primeiro dia civil inteiramente posterior é20/nov, ainda incompleto hoje. Os cinco registros de impressões não dão sua hora individual; não afirmar entrega pós-pausa sem evidência horária por anúncio. Preservar todo o dia19 e as contribuições anteriores dos pausados na série principal.

Melhora agregada18→19: **+1,83p.p., IC95%−3,69a+7,35**. Mesmos dois IDs sobreviventes: **+0,99p.p., IC95%−4,70a+6,69**. Ambos inconclusivos. O anúncio `120252297350870505` passou225→493LPV e `120251541120490505`,277→95LPV; dois IDs constantes não significam pesos, visitantes ou qualidade constantes. Não atribuir o movimento às pausas, às versões de criativo17/nov ou à landing. Nenhuma alteração Meta pelo agente.

Configuração atual versus ontem sem nova edição semântica: original2ACTIVE/3PAUSED, controle1ACTIVE, clone4ACTIVE/2PAUSED e2conjuntosACTIVE; orçamentos150/150/50, drafts0.110atividades paginadas, nenhuma nova relevante posterior à coleta deontem. Controle mantém targeting14/nov e original edição público/copy17/nov. Diferenças brutas de miniatura assinada e campo `status` de conjunto recém-solicitado foram separadas de mudanças reais, com campos comuns comparados porID.

Nos7dias13–19/nov: experimental1465/4111=35,64%, controle1349/3527=38,25%; diferença−2,61p.p.,IC95%−4,78a−0,44. Semanas06–12→13–19/nov: experimental+1,54p.p.(+4,52% relativo), controle+1,48p.p.(+4,02%); diferença entre mudanças+0,06p.p.,IC95%−2,93a+3,06. Campanhas distintas, eventos atribuídos/dependentes e leituras sequenciais impedem conclusão causal, apesar do intervalo nominal7d excluir zero. Baseline36 sem denominador não é amostra estatística.

Clone separado19/nov223LPV/65Leads/R$48,34=29,15%. Seus conjuntos77LPV/13Leads e146LPV/52Leads têm alocação/públicos diferentes, não A/B50–50; não somar ao endpoint original ou inferir canibalização. Revisão clone18/nov: gasto52,65→52,77, impressões10818→10854, cliques303→305, LPV239/Leads72 iguais. Snapshot anterior intacto; originais sem revisão.

## Refinamento concreto de BL-02 — sem implementar junto ao contraste

**Problema:** o módulo superior atual consome espaço antes da oferta; protótipo offline anterior antecipou a oferta/CTA129px sem mudar texto/tamanho do botão. A interpretação futura pode ser contaminada por excluir retroativamente anúncios pausados ou contar um dia misto como24h de exposição uniforme.

**Mudança futura delimitada:** manter somente a compactação mobile do módulo superior já especificada; preservar headline/copy/CTA/contraste então vigente/Pixel/URLs/scripts. Sem adicionar móduloBL-03, prova social ou segunda variável. Risco de foto menor reduzir confiança permanece não medido.

**ICE:** I8/C5/E8, qualitativo e inalterado; a auditoria de fases aumenta qualidade do plano, não confiança emlift. Sem material opcional obrigatório. BL-01 continua condicional a ofertas próprias verificáveis/autorizadas, pedidos23/out pendentes;20.000/estrelas não comprovados, pedido complementar03/nov não repetido.

**Novo guard explícito do plano:**
1. Congelar baseline por regra antes dos resultados e manter endpoint da campanha original com TODOS os anúncios historicamente veiculados. Nunca filtrar a série primária por `effective_status` atual.
2. Registrar timestamp local de cada intervenção e classificar dias mistos. Sensibilidade dos mesmosIDs sobreviventes não substitui o agregado nem garante exposição comparável.
3. Mostrar coberturaLPV/Lead/gasto dos IDs comuns em ambos períodos e a alocação dentro deles; não inventar CVR para células0LPV. Guard aritmético da soma por anúncio deve passar antes da interpretação.
4. Manter clone em série própria; não juntar campanhas por compartilharem HTML/Pixel. Separar versão criativa/público17/nov, targetingcontrole14/nov e fronteira19/nov em sensibilidades documentadas, sem escolher apenas fase favorável.
5. CVRLead/LPV continua primária, CPL secundária; IC95%, cobertura dos dias da semana, volume e consistência pré-planejados. Pesos e dias comuns nas sensibilidades devem ser fixados antes do resultado futuro, não selecionados pelo p-valor.

Este refinamento **não altera4170LPV de planejamento do CRO-002**, cuja revalidação única é somente ao congelar baseline após publicação confirmada. Tampouco cria espera extra depois de convite operacional ou reabre CRO-001.

## Decisão, responsável e observação que resolve o gate

**ibombonato: decidir o PR#16**, atualmente aberto/sem auto-merge. Autenticação e push permission confirmados; não há gateGitHub401 atual. Depois de eventual aprovação/merge humano, exigir PagesSHA+HTML para iniciar avaliação; congelar14dias completos anteriores, excluir dia misto e seguir planoCRO-002. Sem outro experimento enquanto#16 estiver pendente/em avaliação. Próxima análise20/nov completo verifica primeiro dia civil integral após pausas; isso é observação de contexto, não novo requisito arbitrário de publicação.

Produção atual: SHA`4ec19e3ea31a7053bb4a78efa2a6a481c0f09e08`, deployment7940611961success20/nov11:36:39Z, Actions44728901326success; ambosHTMLs públicosHTTP200 byte a byte iguais. Nova alteração humana emcontrole é somenteURLs; não foi feita pelo agente nem reinicia baseline. Proposta preserva tudo além das duas coresCSS deCRO-002.

QA da sincronização20/nov: Chromiumreal390×844/360×800 inspecionado visualmente, extras320×740/1280×900; CTAduaslinhas/inteiro primeira dobra, geometria preservada, foto/seisbenefícios/scroll/focoEntersemfalhas/overflow ouexceçõesJS observadas. NodeVMscriptreal10casos+igualdadehref/constantePASSemprodução/proposta. Meta/WhatsAppbloqueados antes de navegar, timers interceptados sóQA; zeroLeadreal/join/mensagem. NãoSafari/WebVitals/lift.
