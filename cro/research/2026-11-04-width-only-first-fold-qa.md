# BL-02 — Primeira dobra compacta: breakpoint restrito ao mobile

**04/11/2026. Pesquisa offline, não implementação nem CRO-003.** CRO-002 continua Em PR #16/não publicado; CRO-001 permanece encerrado Inconclusivo. A fonte foi a proposta local sincronizada à main atual, incluindo as duas cores de CRO-002 e a alegação externa20.000, que continua não comprovada. Nenhum desses conteúdos foi publicado pelo agente.

## Entrega concreta nova

A lacuna técnica registrada em31/out foi tratada em um protótipo fora do repositório: **acrescentar somente um bloco `@media (max-width: 480px)`**, com overrides do módulo hero/marca/foto/content. Não substituir o breakpoint antigo por altura OU largura, nem alterar os estilos do CTA ou compactar desktop baixo. Remover esse bloco reconstrói a fonte byte a byte; scripts, links, palavras e regras anteriores permanecem íntegros.

**Hipótese:** compactar o módulo inicial pode reduzir a varredura até a oferta e os benefícios. O CTA já era visível; não existe evidência de botão oculto. **ICE mantido I8/C5/E8:** a confiança técnica aumentou, não a confiança em ganho de conversão. Foto128→88px/marca menor ainda podem reduzir confiança pessoal.

## Resultado observado em Chromium real

| Verificação | Resultado no protótipo |
|---|---|
|390×844|Topo CTA503,75→374,75px; altura62px intacta; benefícios inteiros2→4|
|360×800|Topo CTA500,14→371,14px; altura60px intacta; benefícios inteiros0→2|
|320×740|Topo CTA519,97→390,97px; altura60px intacta|
|1024×600 e1280×720, desktop baixo|Geometria, fontes, CTA e screenshots idênticos ao baseline|
|640×450, reflow equivalente a200% de1280×900|Sem overflow horizontal; scroll final, Tab/foco/Enter funcionais; baseline/candidato idênticos|
|Reduced-motion390|Regra existente mantém transition:none/0s; hover instantâneo−2px preservado, sem segunda alteração|

São309 verificações programáticas de escopo/render/interação, não309 testes independentes de CRO. Capturas390/360 também inspecionadas pelo agente principal: headline eCTA sem cortes/colisões; em360 a segunda linha da grade ainda não aparece inteira. Meta/WhatsApp bloqueados antes das navegações, fbq e timer150ms interceptados somente no QA; zero eventos reais ou entrada no grupo. Navegador/servidor/daemon dedicados encerrados. NodeVM separado do script real de produção e proposta:10casos comportamentais e igualdade literalhref/constante passam em cada artefato.

![BL-02 — pesquisa offline390×844, NÃO implementada](../screenshots/research-BL-02-width-only-2026-11-04-390x844.png)

[Pesquisa offline360×800](../screenshots/research-BL-02-width-only-2026-11-04-360x800.png)

## Limitações preservadas

- Reflow foi simulação por viewport CSS, **não zoom real**;195pxCSS/texto ampliado/Safari/dispositivo real/WebVitals não foram testados. Não afirmar conformidade WCAG integral.
- Diagnóstico extra1280×900: geometria igual, mas565pixels diferentes exclusivamente na foto; causa não comprovada. Não alegar PNG idêntico nesse tamanho. Os dois desktops baixos exigidos passaram com identidade de imagem.
- Primeiro diagnóstico confundiu scrollbar vertical15px com overflow; registro falho preservado e execução refeita com `scrollWidth <= innerWidth`. Não relaxar o teste para aceitar overflow positivo.
-129px de antecipação é evidência geométrica, **não lift**. Compreensão e confiança não foram medidas;20.000/estrelas não foram validados pelo QA nem pela autoria humana.

## Plano e próxima decisão

Apenas após decidir/publicar/avaliar e encerrar explicitamente CRO-002, considerar BL-02 como fallback sem material, ou BL-01 se vierem ofertas reais autorizadas. Nenhum ID novo hoje. Futuro teste: uma variável principal de arquitetura mobile, Lead/LPV estável, CPLproxy secundário, baseline do tratamento imediatamente anterior e sensibilidades de mix/IDs conforme plano27/out. Recalcular amostra/checkpoint ao congelar esse futuro baseline; **não substituir o plano14dias/4170LPV original doCRO-002**. Zoom real/texto ampliado e QA da versão final ainda são gates antes de implementação, não motivos para bloquear o contraste já preparado.

Artefatos executáveis/raws/hash-checks: `~/work/hermes-scratch/cro-icb-2026-11-04/bl02-offline/`, incluindo `qa_bl02.py`, `QA-BL02-2026-11-04.json`, `delivery-verification.json`, `NOTA-BL02-2026-11-04.md` eHTMLs offline. Não abrirHTML fora do script protegido; os scripts originais foram preservados. **Sincronização remota desta nota bloqueada por GETGitHub/userHTTP401**, sem tentativa de escrita após a falha. Aprovação doPR e autenticação são gates distintos, encaminhados a ibombonato/@hermes.
