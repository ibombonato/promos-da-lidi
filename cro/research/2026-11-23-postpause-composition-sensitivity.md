# 23/nov — separação entre recuperação observada e efeito do próximo teste

## Evidência nova
MCP oficial e Graph GET atuais conciliados: 156 verificações PASS. A fase posterior às pausas externas de 19/nov 00:08 São Paulo agora cobre três dias civis completos, 20–22/nov. O dia 19/nov continua misto e preservado; não apagar anúncios históricos hoje pausados do endpoint principal.

| Fase | LPV / Leads experimental | CVR | LPV/dia | Gasto/dia |
|---|---|---|---|---|
|2026-11-18–2026-11-18 (1d)|561 / 192|34,22%|561,00|R$144,07|
|2026-11-19–2026-11-19 (1d)|588 / 212|36,05%|588,00|R$154,10|
|2026-11-20–2026-11-22 (3d)|1693 / 649|38,33%|564,33|R$146,15|

**Sensibilidade, não substituição da primária:** mesmos IDs sobreviventes `120251541120490505` e `120252297350870505`: 18/nov 176/502=35,06% →20–22/nov 649/1693=38,33%. Diferença 3,27 p.p., IC95% nominal [-1,50; 8,05]. Cobertura LPV da campanha 89,48% →100,00%; os 59 LPV excluídos da sensibilidade anterior continuam no total principal de 18/nov. Decomposição simétrica: composição -2,34 p.p. + dentro dos anúncios 5,62 p.p.; identidade verificada sem arredondamento. Mesmo ID não garante mesma distribuição/coorte. Um dia versus três, calendário desigual, eventos atribuídos/dependentes e leituras repetidas não permitem concluir benefício das pausas, da copy ou da landing.

## Refinamento concreto de BL-02, sem implementação
- **Problema/evidência:** módulo hero mobile ocupa248px antes da oferta; protótipo offline anterior antecipou CTA129px, sem comprovar abandono ou lift. O diagnóstico atual demonstra por que um aparente rebote agregado não deve ser usado para escolher a referência do próximo teste.
- **Mudança futura objetiva:** compactar exclusivamente o módulo mobile conforme especificação existente; preservar headline, copy, cor aprovada, CTA, links, Pixel e handler. Não somar nova promessa/prova social/rótulo. ICE I8/C5/E8 mantido, confiança não inflada pelo rebote.
- **Critério de avaliação acrescentado:** primária sempre a campanha original completa, incluindo IDs históricos. Mostrar fases externas18/nov,19/novmisto e20/nov em diante com durações/LPVdia/gastodia. Pesos congelados porID só como sensibilidade, divulgando cobertura antes/depois e IDs novos/ausentes; jamais usar só sobreviventes como desfecho. Alta com IC contendo zero ou mudança de alocação não estabelece efeito das pausas/copy/landing.
- **Teste planejado:** somente após disposição/avaliação explícita de CRO-002; registrar baseline da versão imediatamente anterior e MDE/checkpoint próprios, cobertura semanal, IC95%, mix e QA390×844/360×800, desktop baixo e script sem rede. Não herdar4170 como regra universal nem criar nova espera por janela limpa. Nenhum IDCRO atribuído a esta preparação.

## Gate acionável
CRO-002 permanece Em PR#16 há31dias civis, sem publicação. **Responsável ibombonato:** decidir aprovar o teste isolado de contraste ou rejeitá-lo explicitamente. Não falta volume doCRO-001 (encerrado Inconclusivo) nem material para o contraste. Depois de publicação confirmada, aplicar a regra já registrada de14dias completos anteriores/exclusão do dia misto/revalidação única do volume antes de examinar resultados. Não criar experimento paralelo.

Produção SHA`14c019a34b8f908412f6ccc1be03ddd18d5d6de2`, deployment7986433374 success2026-11-22T23:01:35Z, Actions45080870762 success; HTML público de ambas páginas byte a byte igual. PRs humanos64/65 só rotacionaram URLs do controle, não reiniciam Lead/LPV. Integração prospectiva main+head#16 preserva controle/URLs/copy/scripts e altera só duas coresCSS. Fonte experimental idêntica àQA visual20/nov; NodeVM reexecutado emprodução/proposta, sem nova captura ou implementação alegada. Alegação20.000/estrelas ainda não comprovada. Nenhum Meta editado, merge/auto-merge/deploy, Lead real, entrada emgrupo ou mensagem.
