# BL-03 — explicação inline: viabilidade e custo de atenção

**Data:** 2026-11-08. **Natureza:** pesquisa/protótipo exclusivamente offline, não implementação de experimento. CRO-002 continua Em PR #16, sem publicação; CRO-001 permanece encerrado Inconclusivo. Nenhum CRO-003 foi criado.

## Avanço sobre a especificação de 06/nov

A FAQ humana publicada distingue recebimento de ofertas de compra na loja. Essa linguagem fundamentou uma hipótese, mas ainda não havia renderização do módulo. Hoje o candidato foi executado em Chromium real e comparado com a proposta atual de CRO-002, sem modificar o HTML da branch ou o site público. A FAQ não prova objeção dos visitantes, permissões do grupo, veracidade de prova social ou ganho de conversão.

**Problema hipotético:** quem vem do anúncio pode não compreender se entra num grupo para receber links ou se já assume uma compra. Não há entrevista, heatmap ou teste de compreensão demonstrando esse motivo de abandono.

**Uma alteração principal futura:** inserir somente este parágrafo depois do CTA existente e antes da prova social, usando a classe `.copy` já existente, sem CSS extra:

> **Como funciona a compra?** Você recebe ofertas e cupons no grupo. Se quiser comprar, abre o link da oferta e faz o pedido na loja.

Não adiciona link, FAQ externa, CTA secundário, garantia de desconto, regra administrativa ou material artificial. Preserva o caminho anúncio → index3 → CTA → convite e a definição de Lead. A formulação descreve o mecanismo da oferta; ainda não demonstra compreensão pelo usuário.

**Justificativa/resultado esperado:** reduzir incerteza sobre funcionamento e separar adesão gratuita de compra opcional. **Risco:** antecipar a ideia de compra pode aumentar a percepção de compromisso; texto e prova social mais abaixo competem por atenção. Não alegar que texto adicional necessariamente reduz fricção.

**ICE:** impacto6/confiança5/facilidade8, qualitativo e inalterado; confiança é na plausibilidade, não em lift. BL-01 continua prioritário se chegar material próprio verificável; BL-02 permanece o fallback estrutural sem material. Esta pesquisa não promove BL-03 acima de BL-02 nem altera o plano de CRO-002.

## Comparação geométrica real

| Viewport | CTA y / altura, antes e depois | Explicação: y–fim / altura | Início da grade antes → depois | Altura da página antes → depois |
|---|---|---|---|---|
| 390×844 | 503,75 / 62px | 577,75–657,06 / 79,31px | 732,13 → 823,44px | 1068 → 1159px |
| 360×800 | 500,14 / 60px | 572,14–651,45 / 79,31px | 726,52 → 817,83px | 1076 → 1167px |
| 320×740 | 519,97 / 60px | 591,97–691,11 / 99,14px | 746,34 → 857,48px | 1109 → 1220px |
| 1280×900 | 790,89 / 76px | 883,89–981,08 / 97,19px | 1051,64 → 1170,83px | 1399 → 1518px |

**Aprendizado novo:** CTA não é antecipado nem ampliado. No mobile390/360, a explicação cabe integralmente na primeira dobra, mas desloca a grade em91,31px; em360 a grade passa a começar fora da primeira dobra. É um custo de exposição, não um benefício geométrico. Em390 a captura mostra apenas o início das células na dobra. A página fica maior, exigindo mais rolagem. Não combinar com compactaçãoBL-02 para neutralizar esse efeito num mesmo experimento.

A inspeção visual390×844 e360×800 confirmou texto sem corte/colisão, mantendo o botão inteiro e a identidade visual. A alegação20.000/estrelas aparece preservada, **não validada**; comprovação solicitada anteriormente segue pendente. Em360 o título de benefícios encosta no final da captura, mas o scroll chega normalmente ao conteúdo restante. No desktop1280, o novo parágrafo começa abaixo da primeira dobra: não apresentá-lo como exposição garantida para todos.

![Pesquisa offline BL-03 — 390×844](../screenshots/research-BL-03-inline-2026-11-08-390x844.png)

![Pesquisa offline BL-03 — 360×800](../screenshots/research-BL-03-inline-2026-11-08-360x800.png)

## Gates de QA efetivamente executados

- RED: módulo ausente na fonte, asserção esperada registrada. GREEN: remover exatamente a inserção reconstrói a fonte completa byte a byte; CSS, scripts, href/src, CTA e aria-label preservados.
- Oito combinações: baseline/candidato em390×844,360×800,320×740,1280×900. Sem overflow horizontal, foto e seis benefícios carregados, sem exceções JS observadas. Geometria/fonte/fundo do CTA idênticos em cada par.
- Tab/Enter executou uma chamada local interceptada Lead e timer150ms, mantendo URL da prévia; rolagem nativa até o fim e screenshots inicial/final. DomíniosMeta/WhatsApp bloqueados antes de navegar; zero eventos reais, entradas em grupo ou mensagens.
- Script real do candidato executado em NodeVM sem rede:10casos comportamentais e igualdade literalhref/constante aprovados. Fonte da landing na branch permaneceu intacta; arquivos de candidato ficam fora do repositório.
- Chromium em Linux não é Safari real, teste de compreensão, zoom real, WebVitals de campo ou comprovação de conformidade integral. Estados desktop baixo e texto ampliado ainda precisam ser avaliados antes de eventual implementação.

## Plano de teste futuro, não iniciado

Somente após decisão/publicação/avaliação explícita de CRO-002, se BL-03 for selecionado. Confirmar a versão imediatamente anterior, registrar nova hipótese/ID apenas ao implementar, preservar uma variável principal e capturar a versão realmente candidata.

Principal Lead/LPV; secundária CPL. Pré14dias completos imediatamente anteriores à publicação confirmada, exclusão do dia misto; MDE de planejamento+3p.p., alfa bilateral5%, poder80%, volume calculado com esse baseline uma única vez antes de examinar desfecho; cobertura semanal e checkpoint explícito, sem parada por p-valor favorável. Não herdar4170 como limiar universal. Mostrar mix por anúncios/dispositivo/posicionamento, novos IDs e evolução do controle sem substituir a primária agregada nem afirmar causalidade. Não exige fotos/depoimentos/ofertas extras; esses materiais destravam BL-01, não este módulo.

## Contexto de decisão de hoje

Experimental07/nov196/611=32,08%, controle225/582=38,66%; diferença−6,58p.p., IC95%nominal aproximado−12,00a−1,16. Em7dias,35,53%vs37,20%, diferença−1,67p.p.,IC95%−3,63a+0,29. Intervalos descritivos para eventos atribuídos/dependentes; campanhas não randomizadas, múltiplas leituras e mudanças de mix impedem conclusão causal. CRO-002 não publicado não pode explicar essas taxas. Dois anúncios lançados21/out já representam80,20%dosLPV experimentais do dia; não assumir a antiga composição da campanha.

**Bloqueio de publicação documental:** GETGitHub/userHTTP401Badcredentials persiste. Nenhuma escrita remota tentada; ibombonato/@hermes deve restaurar autenticação segura/identidade/permissão, sincronizar PR#16 com main atual e todo histórico local preservado, depois decidir o experimento. Não aprovar a branch remota antiga como se estivesse atualizada. Não foi aberto PR paralelo, realizado merge/deploy ou modificado Meta.

Artefatos atuais sem secrets em `~/work/hermes-scratch/cro-icb-2026-11-08/`: `bl03-offline/qa.json`, candidatos/capturas/RED, `qa_bl03.py`, `cta-offline.json`, `daily-summary.json`, respostasMeta atuais e validações. Screenshots no repositório são artefatos de pesquisa, não exposição pública.
