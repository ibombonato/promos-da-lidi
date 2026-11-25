# 25/nov — primeiro dia completo pós-pausa, nova fronteira de orçamento e entrega ambígua

## Evidência nova e encaminhamentos

MCP oficial e Graph GET atuais: 201 verificações PASS; janelas 24/nov,22–24/nov,18–24/nov,11–24/nov completas em America/Sao_Paulo. Aliases selecionados, não somados. Lead é proxy de clique pré-navegação, não entrada confirmada; campanhas não randomizadas e eventos atribuídos/dependentes.

1. **Clone24/nov, primeiro dia completo após pausas23/nov:** 207LPV/84Leads/R$44,93,CVR40,58%,CPLR$0,53. Campanha/conjuntos/anúncios/horas conciliados; entrega exclusivamente do anúncio120252802517800505/conjunto120252802517710505. Roster atual1ACTIVE/3PAUSED/2ADSET_PAUSED. Preservar23/nov misto e contribuições históricas, não filtrar por status atual. Comparação clone23→24 +6,28p.p.,IC95%[-2,69;+15,26] é descritiva: não prova benefício de pausa, canibalização ou efeito na campanha original. Clone nunca somado ao endpoint original.
2. **Novas edições externas hoje25/nov:** controleR$150→300 às06:43:50SP; cloneR$50→150 às06:44:55SP. Atividades e budgets atuais confirmam; originalR$150 inalterado. Essas edições ocorreram DEPOIS do cutoff24/nov e não explicam retrospectivamente seu CVR/entrega.25/nov é misto,26/nov primeiro dia potencialmente completo pós-orçamento, disponível27/nov09hSP. **Gestor ibombonato:** considerar essas fases ao interpretar próximas leituras; não extrapolar LPV proporcionalmente ao orçamento nem editar Meta por conta deste diagnóstico. Nenhuma mudança Meta feita pelo agente.
3. **Bloqueio de confirmação da entrega24/nov:** execução8f4a1d1d4c3e40f2bd4984f98e01afb3 completed; recibo da ponte `partial_ambiguous`, parte `uncertain`, `TimeoutError`,message_id=null, nenhum evento sent correspondente. Hash da resposta final extraída confere. Não declarar mensagem entregue ou não entregue: timeout pode ocorrer após aceite. **Operador @hermes:** reconciliar esse handle no transporte autorizado antes de qualquer reenvio, preservando deduplicação; não reenviar automaticamente. Histórico23/out profile_parked está resolved, não é causa atual demonstrada. Scheduler ativo não resolve recibo ambíguo. Entrega dehoje depende da conclusão e recibo posteriores. Sem envio direto/reconfiguração de outros perfis.

## Refinamento concreto de BL-02 — ICE I8/C5/E8 mantido

- Problema/evidência: hero mobile248px antecede oferta; protótipo offline anterior antecipou CTA129px. Isso sustenta viabilidade de teste, não abandono/compreensão ou lift.
- Mudança futura: compactar somente arquitetura do módulo mobile, preservando headline/copy/CTA/contraste vigente/handler/links/Pixel. Não requer material novo; sem promessas ou prova social inventadas.
- **Novo caso de aceitação:** distinguir fase de pausa do clone23/nov da fase posterior de orçamento25/nov; tabelas por campanha/conjunto/dia, com budgets e duração inclusiva explícitos. Manter primária da campanha original inteira com todos IDs históricos, nunca pooling clone nem comparação de totais de durações diferentes. Alteração de orçamento ocorrida hoje não deve ser projetada sobre ontem.
- Manter CVR primária/CPL secundária, pesos pré-fixados e coberturas por anúncio/dispositivo como sensibilidades separadas, nunca soma marginal causal. Regra do pré-período não pode ser escolhida por taxas favoráveis. Amostra/MDE próprios só ao implementarBL-02 após avaliar/encerrarCRO-002, sem herdar4170 universalmente.
- Gate atual: decisão humana sobrePR16; nenhum tratamento paralelo. Se publicarCRO-002, aplicar plano pré-registrado e avaliar/encerrar antes do seguinte. Não reabrirCRO-001 ou criar espera por volume já encerrado. Projeção eventual usa tráfego original observado, não novos orçamentos de outras campanhas.

## Integridade e QA

ProduçãoSHA`bbd83c30c6e8b33f4ce11f8829fefaeef55ff5a7`,deployment8056833291success2026-11-25T12:01:38Z,Actions45609737630success; ambas landings públicas HTTP200/byte a byte iguais àmain. Contraste antigo ainda público, portantoCRO-002não publicado. Humanos#71/#74 mudaram somenteURLscontrole/experimental; rotas atuais preservadas. Integração localmain+head#16 difere exclusivamente nas duascoresCSS; controle/scripts/copy/links iguaisàmain. Alegação20.000/estrelas continua não comprovada, pedidos anteriores pendentes, sem nova cobrança.

QA atualChromium390×844/360×800 e extras320×740/1280×900, capturas mobile inspecionadas visualmente pelo agenteprincipal: botão legível em duas linhas, inteiro na primeira dobra, mesma geometria503,75–565,75/500,14–560,14px. Foto/seisbenefícios/scroll/focoEnter íntegros, semoverflowhorizontal/cortes/exceçãoJS. NodeVM10casos+igualdadehref/constantePASS emprodução/proposta; Meta/WhatsAppbloqueados antesdenavegar, zeroLeadreal/join/mensagem. NãoSafari/WebVitals ou ganhoCVR.

Limitação da coleta: uma consulta MCPsuplementar deconjuntos24/nov foi repetida com o mesmo nome antes do snapshot; resposta inicial indisponível, sem afirmar identidade/ausência de revisão dela. Resposta final conciliada independentemente; raws principais e falhas iniciais preservados. Célula iPadcontrole1LPV/2Leads preservada, ICbinomial não estimado nessa célula; não truncar métricas atribuídas para impor modelo binomial. Totais principais exatos.

CRO-002 há33dias desdepreparação: **ibombonato decidirPR16**, não falta amostra/material. Semmerge/auto-merge/deploy ouCROnovo.
