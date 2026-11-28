# BL-02 — Primeira dobra compacta: viabilidade exploratória medida

**Data:** 2026-10-31. **Estado:** pesquisa offline, não implementação de experimento, não CRO-003. CRO-002 segue Em PR #16, não publicado. Nenhum candidato deste documento foi aplicado a `index3.html` ou exposto aos visitantes.

## Entrega nova

A estimativa de 24/out foi transformada em protótipo renderizado: cabeçalho136px/foto88px/content-padding34px, marca34/26px, ornamentos redimensionados. Base offline = desenho do PR CRO-002, com suas duas cores de contraste; não confundir com a produção de cores antigas. Mesmo corpo HTML, headline, copy, CTA inteiro/dimensões, prova social existente, links e JavaScript. O material foi gerado fora do repositório, em `~/work/hermes-scratch/cro-icb-2026-10-31/preview/`; o PR recebe somente documentação e capturas de pesquisa.

Na primeira renderização, o ornamento `.shape.one` conservou210px e invadiu visualmente a área da headline após a compactação. **Falha observada, corrigida apenas no protótipo:** limitar dimensões/posição dos dois ornamentos no breakpoint. Capturas finais reinspecionadas390×844/360×800/320×740: headline livre, marca e foto separadas, CTA íntegro. Isso acrescenta um guard concreto à especificação futura: verificar o contorno transformado dos ornamentos, não somente caixas de conteúdo.

## Medidas reais antes → candidato

| Medida | 390×844 | 360×800 | 320×740 |
|---|---|---|---|
| Hero | 248→136px | 248→136px | 248→136px |
| Topo do CTA | 503,75→374,75px | 500,14→371,14px | 519,97→390,97px |
| Altura do CTA | 62→62px | 60→60px | 60→60px |
| Topo da grade | 732,13→603,13px | 726,52→597,52px | 746,34→617,34px |
| Células de benefícios inteiras na primeira dobra | 2→4 | 0→2 | 0→2 |

Avanço129px confirmado, sem reduzir fontes da oferta/CTA. Em360, a segunda linha de benefícios ainda termina abaixo da dobra; não declarar seis benefícios visíveis. Em1280×900, geometria e screenshot antes/depois idênticos byte a byte. **Limite:** o breakpoint herdado usa `(max-height:760px) OR (max-width:480px)`; o protótipo não foi validado em desktop baixo. Antes de um experimento mobile-only, separar o override por largura e validar desktop baixo, zoom/texto ampliado e reduced-motion. Viabilidade nas viewports testadas não significa QA integral de uma implementação futura nem testeSafari/WebVitals.

![Pesquisa offline BL-02 390×844 — NÃO implementado](../screenshots/research-BL-02-offline-390x844.png)

[Pesquisa offline360×800](../screenshots/research-BL-02-offline-360x800.png)

## Hipótese e prioridade

**Problema hipotético:** área inicial de marca exige mais varredura antes da oferta e deixa benefícios fora da primeira dobra. O CTA já está visível hoje; não há evidência de botão escondido.

**Mudança objetiva candidata:** compactar um único módulo de hierarquia mobile, preservando autoria/foto e todas as palavras/ação. Não misturar com CTA compacto, prova social ou exemplos de ofertas. **Comportamento esperado:** entender proposta/benefícios com menos varredura; somente Lead/LPV posterior pode verificar ganho.129px ou mais células visíveis não são aumento de CVR.

**ICE mantido I8/C5/E8:** viabilidade geométrica ganhou evidência, confiança comportamental não. Risco: foto128→88px e marca menor podem reduzir confiança pessoal. BL-01 continua prioritário se chegarem três ofertas próprias reais/autorizadas; sem material, BL-02 é fallback. Pedido23/out e comprovação16.000/estrelas continuam pendentes, sem nova cobrança ou validação por aparecer noHTML.

## Plano e gates

1. Primeiro decidir/publicar/avaliar e encerrar explicitamente CRO-002, sem tratamento paralelo. Hoje não falta amostra do CRO-001: ele está encerrado Inconclusivo.
2. Futuro baseline somente do tratamento imediatamente anterior; regra7dias completos e ampliação para trás dentro desse tratamento se necessária. Confirmar PagesSHA+HTML, excluir dia parcialmente exposto, registrar anúncios/orçamento/atribuição. Não mudar o plano14dias/4170 de CRO-002 com esta pesquisa.
3. Lead/LPV principal e CPLproxy secundário, MDE de planejamento+3p.p.; recalcular amostra/checkpoint uma vez ao congelar baseline. Mesma primária agregada e sensibilidade pré-especificada por anúncios/IDs comuns/cobertura; IC95% descritivos, controle contextual não randomizado. Encerrar Inconclusivo se necessário, não prolongar por significância.
4. Validar as lacunas acima e QA mobile real antes de qualquer implementação/ID. Screenshot deste documento é pesquisa, não artefato de um CRO publicado.

**Segurança executada:** Meta/WhatsApp bloqueados antes de navegar; scroll/foco/Enter aprovados nas quatro viewports, chamadaLead e timer150ms interceptados localmente, zero eventos reais ou entrada no grupo. Sem exceçõesJS observadas. NodeVM do script real:10casos comportamentais passam emprodução/PR/offline, igualdade literalhref/constante falha pela query operacional já encaminhada; nenhuma URL foi normalizada para ocultar essa ressalva. Artefatos atuais: `BL-02-replacements.json`, `BL-02-exploratory-mobile.json`, capturas antes/depois e `today-validation.json` no diretório desta execução.
