# Auditoria de preservação de rota — 26/10/2026

**Entrega concreta:** diagnóstico reproduzível de uma divergência introduzida externamente, com encaminhamento ao responsável; não é novo experimento, alteração de destino ou resultado de CRO. CRO-002 continua Em PR #16. CRO-001 está encerrado Inconclusivo.

## Evidência atual

- Origin/main e Pages `c8a16941814a43a040506a5330903587e5c16852`; build `built`, concluído em 26/out/2026 02:08:45Z (25/out 23:08:45 São Paulo). Ambas as landings públicas HTTP200 e byte a byte iguais ao commit.
- Entre a main verificada ontem `a348725` e a atual, as mudanças de `index3.html`/`index4_li.html` são somente valores de URLs operacionais. HTML inteiro, após mascarar exclusivamente esses valores, idêntico; CSS, copy, Pixel, evento e handler não mudaram. O agente não escolheu nem modificou as rotas.
- Commit externo [`a77f34b5fab43a1ff1ed8efd1b586d9918fd2664`](https://github.com/ibombonato/promos-da-lidi/commit/a77f34b5fab43a1ff1ed8efd1b586d9918fd2664), 26/out 00:53:18Z (25/out 21:53:18 São Paulo), passou a usar o mesmo código de convite, mas URLs literais diferentes:

| Caminho | Valor atual |
|---|---|
| `href` no HTML / fallback sem JavaScript | `https://chat.whatsapp.com/IUVoXlESwSh5ke4ROZRBWx` |
| `WHATSAPP_GROUP_URL` | `https://chat.whatsapp.com/IUVoXlESwSh5ke4ROZRBWx?s=cl&p=a&mlu=4&ilr=4` |

**Com JavaScript, `whatsappCta.href = WHATSAPP_GROUP_URL` reescreve o link já no carregamento.** Não ocorre apenas no clique normal: cliques modificados usam o href reescrito. Sem JavaScript, permanece a URL sem query. Origem e caminho/código do convite são iguais; diferenças de query **não foram tratadas como destino de grupo diferente ou falha comprovada do WhatsApp**. Não há evidência de parâmetros inválidos, grupo cheio ou perda de participantes. A semântica desses parâmetros no WhatsApp não foi validada; não remover, copiar ou normalizar por suposição.

## Testes realmente executados

1. Guard de escopo CRO-002: PASS. Aplicar somente as duas cores CSS pré-registradas à main atual reproduz o candidato inteiro byte a byte; scripts, recursos, links e controle preservados.
2. Harness anterior com exigência de igualdade literal `href === WHATSAPP_GROUP_URL`: **FAIL**, na main e por consequência no candidato que a preserva. Não apresentar o antigo total de 11 aprovações como QA atual íntegra.
3. Auditoria comportamental separada em Node VM, sem rede, executando o handler real da fonte publicada e do candidato: **10 casos PASS** (normal com tracking, ausente, lançando erro; Ctrl/Meta/Shift/Alt; central/direito; evento já cancelado). Confirmou reescrita no carregamento, Lead capturado antes do timer/navegação normal e delay150ms. No erro de tracking, redirecionamento imediato já existente é preservado. Esses passes não resolvem a divergência literal nem verificam a entrada no grupo.
4. Zero eventos Meta reais, navegações WhatsApp, mensagens ou entradas no grupo. Não há nova alteração visual: screenshots390×844/360×800 do CRO-002 continuam representativos do desenho, confirmado por substituição exata; não são nova validação Safari ou de parâmetros WhatsApp.

Artefatos locais: `~/work/hermes-scratch/cro-icb-2026-10-26/cta-production.json`, `cta-pr.json`, `cta_runtime_audit.cjs`, `condensed-evidence.log`, `test_scope.py` e `live-validation.json`.

## Encaminhamento e decisão

**Responsável: ibombonato. Ação solicitada:** confirmar se a diferença entre o fallback sem query e a URL JavaScript parametrizada é intencional e qual forma deve permanecer na próxima manutenção operacional. Se desejar uniformização, ela exige autorização explícita de destino/parâmetros; não será embutida no experimento de contraste. O diagnóstico e esta solicitação constam no mesmo PR#16 e no relatório diário, sem criar PR experimental paralelo.

**Efeito na medição:** não reiniciar o baseline do clique Lead/LPV; handler/evento pré-redirecionamento e tratamento visível não mudaram. Registrar eventual impacto posterior ao clique como desconhecido, não como lift ou queda causada pela landing. O principal gate de CRO-002 continua decisão humana no#16 e confirmação PagesSHA+HTML após publicação; a divergência de URL é uma ressalva operacional/QA para decisão do responsável, não justificativa para esperar arbitrariamente mais LPV.

**Integridade do PR:** main atual incorporada localmente com ancestralidade, preservando literalmente convites e parâmetros atuais. Diff de `index3.html` contra main mantém só as duas cores de contraste; `index4_li.html` idêntico à main. Sem correção automática, merge remoto, auto-merge, deploy ou mutação Meta. Prova social16.000/estrelas ainda sem comprovação; pedido de materiais de23/out permanece pendente, sem nova cobrança.
