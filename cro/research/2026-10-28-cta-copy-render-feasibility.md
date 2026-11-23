# BL-06 — Viabilidade mobile do rótulo compacto, sem exposição pública

**Data:** 28/10/2026. **Estado:** pesquisa exploratória local; não é CRO-003 nem alteração da landing do PR. CRO-002 continua Em PR #16, não publicado. Complementa a hipótese de25/out, sem alterar plano/checkpoint ou sobrepor tratamentos.

## Pergunta resolvida hoje

A redução de34para22caracteres faz o comando caber em uma linha **sem nenhum ajuste CSS**? A especificação anterior corretamente não afirmava isso antes da renderização. Agora foram comparados arquivos locais derivados exatamente do HEAD `9fb05df2914ea48f06042a2c5ab862479bc7fb86` doPR#16: baseline com contraste proposto e candidato com **somente** a substituição literal `ENTRAR GRÁTIS NO GRUPO DO WHATSAPP` → `ENTRAR GRÁTIS NO GRUPO`. Essa escolha isola texto na preparação e não presume publicação do contraste. O candidato não substituiu `index3.html` no repositório, PR ou produção.

## Resultado observado em Chromium real

| Viewport | Linhas baseline→candidato | Altura CTA antes→depois | Topo CTA antes/depois | Largura CTA |
|---|---:|---:|---:|---:|
|390×844|2→1|62→56px|503,75px|346px|
|360×800|2→1|60→56px|500,14px|316px|
|320×740|2→2|60→60px|519,97px|276px|
|1280×900|2→1|76→64px|790,89px|458px|

- Screenshots baseline/candidato390×844e360×800 **inspecionados visualmente**: rótulo e ícone íntegros, alinhados, botão inteiro na primeira dobra; headline mantém “NO SEU WHATSAPP”. Sem overflow horizontal nos quatro viewports.
- A troca textual não antecipa o **topo** do botão; economiza apenas6px/4px de altura em390/360. Portanto não vender esta hipótese como reorganização relevante da primeira dobra ou substituto doBL-02. Em320px o rótulo continua em duas linhas; não prometer resultado universal.
- O ícone e `aria-label="Quero entrar no grupo VIP Promos da Lidi no WhatsApp"` foram preservados. Isso não comprova entendimento de quem lê somente o texto visível: retirar “WhatsApp” do botão continua sendo risco real.
- Foto e seis benefícios carregados; rolagem até o fim e foco/Enter exercitados nos quatro viewports. Enter capturou apenas uma chamada local `['track','Lead']` e timer150ms; a navegação permaneceu local e o timer não foi executado. Nenhuma exceçãoJavaScript observada.
- DomíniosMeta/WhatsApp bloqueados **antes** da navegação; não houve eventoLead real, entrada em grupo ou mensagem. Chromium em Linux com viewport emulado não é Safari real nem WebVitals de campo. Não houve teste de compreensão com usuários nem medição de conversão desta copy.

### Capturas exploratórias, não implementação

![BL-06 — prévia offline390×844, não publicada](../screenshots/research-BL-06-offline-390x844.png)

[Prévia offline360×800](../screenshots/research-BL-06-offline-360x800.png). O baseline visual usado é o mesmo desenho já registrado nas [capturasCRO-002](../screenshots/CRO-002-mobile.png), com o rótulo longo. Cores escuras pertencem ao contraste ainda pendente doPR#16; não são evidência de publicação nem nova hipótese de cor.

## Decisão de priorização atualizada

**ICE mantido I5/C4/E9.** A viabilidade de renderização foi confirmada em360/390, mas a confiança de ganhoCVR não aumenta por isso. BL-06 continua abaixo deBL-01 com material real eBL-02 sem material. SemCSSextra para forçar uma linha em320px; isso adicionaria outra variável. Não implementar enquantoCRO-002 estiver pendente/emavaliação. Pedido23/out para ofertas reais e comprovação16.000/estrelas continua pendente, sem cobrança repetida; o print da página não valida essas alegações.

**Hipótese futura:** reduzir redundância visual mantendo ação/gratuidade/grupo pode facilitar leitura do comando; o risco inverso é reduzir clareza do canal. Testar apenas o rótulo, depois de resolver/avaliarCRO-002 e revalidar prioridade. Preservar headline, arquitetura, cores então vigentes, scripts, Pixel, destinos e nome acessível.

**Plano futuro preservado:** Lead/LPV como primária e CPLproxy secundária; publicaçãoPagesSHA+HTML e dia misto excluído; baseline da versão imediatamente anterior, MDE/checkpoint/amostra calculados antes do pós, cobertura semanal, IC95% descritivos e sensibilidades de mix. Não usar diminuição de caracteres/linhas como substituto de conversão; não reciclar4170LPV automaticamente ou selecionar segmento favorável. Nova edição externa do orçamento do controle em27/out exige fase de transição explícita, sem mudar a métrica ou tratar campanhas distintas como randomizadas.

**Artefatos reproduzíveis:** `/home/ibombonatohermes/work/hermes-scratch/cro-icb-2026-10-28/`: `preview/baseline.html`, `preview/candidate.html`, `preview_qa.py`, `BL-06-exploratory-mobile.json`, oito capturas originais. Guarda de substituição única confirmou que remover somente a alteração textual reconstrói integralmente o baseline. `index3.html` doPR mantém exclusivamente as duas coresCSS doCRO-002 contra main; controle/scripts/convites inalterados.
