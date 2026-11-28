# 2026-11-10 — Clone pausado, rascunho novo e integridade do próximo teste

## Entrega e decisão

Auditoria read-only de uma nova campanha e de uma nova pendência no Ads Manager, separando configuração persistida, rascunho e entrega observada. Nenhum novo tratamento, ID CRO ou mudança Meta. CRO-002 continua Em PR #16; CRO-001 continua encerrado Inconclusivo. Histórico/esta nota são locais: GET GitHub /user HTTP401 Bad credentials, sem tentativa de escrita remota.

## Evidência nova verificável

- Campanha `120252642171330505`, “LEAD - Grupos - Clone index3 — ICB”, criada 09/nov/2026 às21:35:31 São Paulo, orçamento configurado R$50/dia, atualmente PAUSED. Conjunto `120252642175430505` e anúncio `120252642196110505` também configurados/efetivamente PAUSED. Não confundir com experimental `120250764485030505`, que continua ACTIVE/R$150 e com os mesmos quatro anúncios ativos.
- MCP consultado na mesma conversa/sessão: clone com gasto0/impressões0, LPV/Lead/cliques **null**, não zero medido. Graph GET diário09–10/nov retorna `data:[]`; não há linhas de entrega retornadas nessa janela, cujo dia10 é parcial. Nenhuma contribuição do clone foi adicionada aos totais das duas campanhas. Nenhuma evidência de que tenha causado a diferença atual de CVR.
- Criativo persistido do clone `1468869805218832`, CTA SEE_DETAILS, seis bodies/dois titles, Pixel1504398471438133. Usa post `1226911970510093_122129359023416337`; o endpoint do post retornou Graph code10/permissão. **Destino efetivo não confirmado**: nome “index3” e UTM não provam a URL. Não requisitar mais permissões nem ativar para testar.
- Atividades GET08–10/nov:35 registros, paginação esgotada; filtragem inclui os IDs novos e o conjunto mesmo quando extra_data o chama campaign_id. Criação, edição de targeting e trocas de criativo pertencem ao clone pausado, não à campanha experimental original.
- Continuação obrigatória read-only do MCP mostrou quatro rascunhos, antes três. Novo: anúncio original ativo `120251541120490505`, atualizado09/nov21:58:47SP. Diff staged old→new contém `media_sourcing_spec.bodies`2→7 e `object_story_id`→null. `asset_feed_spec.bodies` permanece2; não dizer que sete variações passaram a veicular.
- GET atual do criativo original `2214895639068786` confirma as duas bodies, título, linkindex3, UTMs e effective_object_story_id já observados. Roster/configuração ativa/conjuntos idênticos àvéspera. Os outros três rascunhos são idênticos ao snapshot anterior. A nova pendência **não é evidência de publicação ou causa da queda**.
- Guard inicial de igualdade do object_story_id falhou: Graph omite esse campo, enquanto effective_object_story_id permanece `104134247643652_1383503420433098`, igual aos dois lados do rascunho. Falha preservada em `strict-story-id-failed-diagnostic.json`; ausência de um campo não demonstra aplicação da edição. Nenhum publish/activate executado.

## Diagnóstico da medição e prioridade

09/nov: experimental225/634=35,49%, controle245/640=38,28%. 03–09/nov:1584/4550=34,81% versus1662/4509=36,86%; diferença−2,05p.p., IC95% nominal aproximado−4,02a−0,07. Quatorze dias:36,26% versus37,75%, diferença−1,49p.p., IC95%−2,89a−0,10. Não escolher estes endpoints como prova causal após leituras diárias; são campanhas distintas, eventos atribuídos potencialmente dependentes, tráfego/mix não randomizado. Não são resultados do contraste não publicado.

Semanas27/out–02/nov→03–09/nov:experimental−3,00p.p./−7,94%relativo,controle−1,70p.p./−4,40%; diferença entre mudanças−1,31p.p., IC95%−4,11a+1,49. Ambas caíram; diferença semanal das evoluções relativas−3,54 pontos percentuais. Baseline36% sem denominador permanece somente referência histórica.

Ad-day08→09/nov: queda experimental−1,28p.p.=+0,08composição−1,36dentro dos anúncios, identidade reconciliada. Anúncios lançados21/out respondem por516/634LPV=81,39%,171Leads; established54/118=45,76%, amostra pequena. Decomposição é aritmética, não causa nem recomendação de alterar ads.

## Encaminhamento concreto ao responsável

**ibombonato/gestor autorizado:** confrontar a pendência nova do anúncio120251541120490505 com o live antes de qualquer publicação manual em lote; não presumir que pertence apenas ao clone pausado. Se decidir futuramente ativar o clone, verificar o destino efetivo do post e registrar o primeiro dia/hora de entrega para segmentação. Não foi feita solicitação de ativação ou alteração de orçamento.

**ibombonato/@hermes:** restaurar autenticação GitHub segura, confirmar identidade/permissão e sincronizar PR#16 com main atual e toda documentação local01–10/nov; só depois decidir o experimento. Branch remota ainda contém alegação16.000/convite antigo, enquanto main contém20.000/rota atual. Não aprovar como se sincronizada; não reverter ou endossar a alegação.

## Próxima hipótese preparada, sem exposição simultânea

BL-02 permanece fallback sem material: compactar exclusivamente módulo da primeira dobra mobile, sem mudar headline/copy/CTA/cor/tracking. ICE8/5/8. Evidência anterior: protótipo avança CTA129px; risco de menor foto/confiança e gates de texto ampliado/zoom reais preservados. Novo refinamento: antes da futura publicação, conferir tanto novos IDs de campanhas quanto rascunhos dos anúncios **já ativos**, com horário de primeira entrega/edição efetivamente publicada; não registrar mera descoberta do draft como mudança live.

Manter primária agregada Lead/LPV; pesos pré-fixados por anúncio e cobertura de smartphones como sensibilidades separadas, sem somar ajustes marginais. Se houver nova entrega real, preservar endpoint e adicionar fase, sem excluir dias desfavoráveis ou reiniciar por convite. Não criar janela arbitrária por este clone pausado. CRO-002 conserva regra14dias pré-publicação/dia misto excluído/revalidação única da referência4170, não novo limiar calculado diariamente.

Pedidos23/out de três ofertas reais autorizadas e comprovação20.000/estrelas complementada03/nov seguem pendentes; não repetir pedido nem bloquear contraste por material opcional.

## QA, publicação e operação

Pages SHA `ab142e82527029473ff3adadaca8ddc98b78273a`, deployment7674620136success10/nov05:44:49Z e Actions42763950380success; ambas landings públicas HTTP200/byte a byte iguais àmain. Mudanças humanas desde ontem apenas convites emindex3/index4_li, verificadas por diff; não reiniciam medição de Lead. Verde antigo emprodução. Candidato local versusmain sóduascoresCSS; scripts/links/copy/controle preservados. NodeVMprodução/proposta10casos+igualdadehref/constantePASSemcada, semrede/eventosMeta/join. Sem nova implementação visual; screenshots originais doPR não são novaQA/Safari/WebVitals.

Execução09/nov `ec4e7bd220c0486b94750e851f1ff6b8` concluída12:08:40Z; ponte aceitou Telegramrecibo19990às12:10:39Z, handle/ID/SHA256daresposta final extraída conferidos. Falha23/out não é oestado atual. Entrega10/nov só verificável após conclusão, semenvio próprio ou alteração deagenda/perfil.

Raw atuais e guards: `~/work/hermes-scratch/cro-icb-2026-11-10/` (analysis.json,today-validation.json,new-clone-and-mix-diagnostic.json,draft-vs-live-verified.json,MCP/Graph/atividades/Pages/live/CTA). Nenhum ganho de conversão alegado.
