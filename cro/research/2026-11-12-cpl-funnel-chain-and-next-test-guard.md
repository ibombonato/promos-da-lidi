# BL-02 — Separar custo de tráfego e resposta da landing na próxima avaliação

**Data:** 2026-11-12. Entrega analítica e refinamento de hipótese, não implementação nem novo ID CRO. CRO-002 continua Em PR #16, não publicado. Documento LOCAL: autenticação GitHub retorna HTTP401 no GET /user; `gh auth status` também confirma ausência de login. Nenhuma escrita remota tentada.

## Evidência específica nova

Duas semanas completas não sobrepostas, com todos os dias da semana: **29/out–04/nov → 05–11/nov/2026**, America/Sao_Paulo. Totais MCP conciliados exatamente com Graph diário; consultas adicionais atuais por anúncio, dispositivo e posicionamento conciliadas separadamente em cada semana. Lead é proxy do clique pré-navegação, não participante confirmado. A alegação externa16.000→20.000 foi publicada em02/nov, dia misto presente na primeira semana; comparações não isolam esse conteúdo, distribuição ou efeitos externos.

| Indicador | Experimental antes → depois | Controle antes → depois |
|---|---:|---:|
| Investimento | R$1.150,92 → R$1.057,97 | R$1.021,86 → R$1.055,43 |
| Impressões | 197415 → 164952 | 266269 → 208550 |
| Cliques no link | 5673 → 5217 | 5801 → 5057 |
| LPV | 4784 → 4332 | 4853 → 4257 |
| Leads proxy | 1780 → 1510 | 1808 → 1564 |
| CPM | R$5,83 → R$6,41 (+10,01%) | R$3,84 → R$5,06 (+31,87%) |
| CTR de link | 2,87% → 3,16% (+10,06%) | 2,18% → 2,42% (+11,30%) |
| LPV/clique | 84,33% → 83,04% (−1,53% relativo) | 83,66% → 84,18% (+0,62%) |
| CVR | 37,21% → 34,86% (−2,35p.p.; −6,32% relativo) | 37,26% → 36,74% (−0,52p.p.; −1,38%) |
| CPL proxy | R$0,6466 → R$0,7006 (+8,36%) | R$0,5652 → R$0,6748 (+19,40%) |

A identidade `CPL = CPM / (1000 × CTR_link × LPV/clique × Lead/LPV)` foi testada numericamente antes de arredondar. Decomposição multiplicativa em logaritmos conserva a identidade: na experimental, CPM e CTR de link praticamente se compensam; CVR menor e, em menor magnitude, LPV/clique menor pressionam o CPL. No controle, o CPM cresceu muito mais do que o CTR, apesar da pequena mudança de CVR. **CPL pior nas duas campanhas não demonstra piora igual da landing nem efeito de um contraste ainda não publicado.** São identidades aritméticas, não estimativas causais dos componentes do leilão ou do carregamento.

Diferença entre mudanças de CVR **−1,83p.p., IC95% nominal aproximado−4,63 a+0,96**; diferença entre evoluções relativas−4,93 pontos percentuais. Intervalos binomiais são aproximações para eventos atribuídos/dependentes; campanhas não randomizadas e consultas sequenciais limitam inferência. Não escolher esta comparação como endpoint de um experimento que não começou.

## Mix e limites de interpretação

- Decomposição simétrica por anúncio da queda experimental−2,35p.p.: **−0,97p.p. composição e−1,38p.p. dentro dos anúncios**. Mesmos quatro IDs com LPV nas duas semanas; identidade exata. Não concluir que o mix explica toda a queda ou que as variações internas pertencem à landing.
- Android smartphone experimental **1251/3130=39,97% →1008/2759=36,53%**; iPhone **527/1649=31,96% →501/1570=31,91%**. A variação semanal não sustenta apontar Safari como causa. Preservadas células pequenas/zero-LPV sem imputação de taxas; sem combinar decomposições marginais como ajuste conjunto.
- Instagram Stories experimental **1421/3876=36,66% →1192/3491=34,14%**. Não usar desempenho dos segmentos como prova causal ou sugestão para editar posicionamentos.
- Todos os breakdowns mantêm contagens exatas. Resíduos monetários preservados com precisão original e inferiores a um centavo; primária MCP/Graph diária exata. Não arredondar cada linha antes de conciliar.

## Refinamento objetivo do próximo teste BL-02

**Problema:** julgar uma mudança de primeira dobra somente por CPL pode confundir custo/distribuição do tráfego com a resposta ao conteúdo. Há uma redução verificável de CVR experimental, mas sua origem não foi isolada.

**Mudança futura delimitada:** somente compactação mobile width-only já prototipada, antecipando oferta/CTA em129px, mantendo headline, copy, links, handler, Pixel e contraste da versão então aprovada. Não acrescentar explicação inline, mudar rótulo ou alterar anúncios junto.

**Justificativa/impacto esperado:** tornar oferta e benefícios acessíveis com menos rolagem; efeito esperado é sobre Lead/LPV, não redução garantida do CPM. Renderização prova viabilidade geométrica, não compreensão ou lift.

**ICE:** I8/C5/E8, mantido; não aumentar confiança pelo diagnóstico observacional.

**Plano acrescentado antes da implementação:**
1. Preservar CVR agregada como primária e CPL como secundária, com baseline/checkpoint próprios definidos ao iniciar o futuro teste.
2. Em cada comparação pré/pós completa, apresentar também CPM, CTR de link e LPV/clique, com identidade de CPL verificada. Se CPL melhorar com CVR inalterada e CPM menor, não chamar isso de vitória da primeira dobra; se CVR melhorar e CPL subir por CPM, registrar sinais distintos e incerteza, sem ignorar o custo nem trocar a primária.
3. Manter sensibilidades de anúncio/calendário/dispositivo com pesos/cobertura previamente definidos e amostra completa; IDs novos/ausentes, células não estimáveis e alterações externas explícitos. Não somar parcelas marginais nem remover dias desfavoráveis.
4. Este refinamento NÃO altera a regra14dias pré-publicação, exclusão do dia misto ou referência original4170LPV do CRO-002. Não cria janela limpa extra e não autoriza teste paralelo. Zoom real/texto ampliado e diferença de foto desktop continuam gates de QA antes de eventual implementação do BL-02.

## Exposição e encaminhamento

Consulta draft explícita no MCP, na mesma sessão/conversa, confirma os mesmos quatro rascunhos, sem adição/remoção ou diferença de conteúdo em relação a11/nov. Configuração live dos anúncios ativos/conjuntos/atribuição continua igual. Clone120252642171330505 e filhos PAUSED; Graph09–11/nov sem linhas, não valores null convertidos em zero. Destino efetivo permanece não confirmado; sem inferir pelo nome, ativar ou publicar.

Novos PRs operacionais#38/#39 mudam somente href/constante da experimental/controle, respectivamente; ambos propõem o mesmo convite, mas continuam pendentes. Não incorporar esses convites antes de decisão humana nem presumir publicação/capacidade do grupo. PR#31 anterior continua aberto. Rotação futura apenas deURLs não reinicia Lead/LPV; membros confirmados de um grupo compartilhado não se tornam atribuíveis a cada campanha.

**Gate humano real — ibombonato/@hermes:** restaurar autenticação segura GitHub, confirmar identidade/permissão de escrita, sincronizar o PR#16 com main atual e histórico local01–12/nov e só então decidir. Branch remota ainda contém16.000/convite anterior; não tratá-la como atualizada. PR#16 aberto/headf9286a3/semmerge/auto-merge, zero comentários/reviews. Publicação atualab142e8 confirmada por deployment7674620136success, Actions42763950380success e HTML público das duas landings byte a byte igual. Verde antigo continua publicado. Nenhuma escrita remota, merge, deploy ou mudança Meta foi feita.

Pedidos de ofertas reais23/out e comprovação agregada/datada/deduplicada20.000/estrelas03/nov continuam pendentes; não repetidos como requisito para contraste/compactação.

**Proveniência:** `~/work/hermes-scratch/cro-icb-2026-11-12/`: funnel-chain-diagnostic.json, chain-*-raw.json, mcp-explicit-drafts-result.json, draft-differences.json, clone-current.json, analysis.json, today-validation.json, summary.log. Nenhum novo HTML/CSS: não foi realizada nova QA visual, e as capturas mobile do PR permanecem as originais. NodeVM atual da produção/proposta: igualdade href/constante e10casos comportamentais aprovados em cada, sem rede, eventos Meta reais ou entrada WhatsApp.
