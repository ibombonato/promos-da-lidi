# BL-06 — Reduzir esforço de leitura do rótulo do CTA

**Data:** 2026-10-25. **Estado:** hipótese de backlog especificada; não implementada, não é CRO-003. CRO-002 permanece o único experimento em PR (#16). Não modifica seu tratamento, baseline ou checkpoint.

## Evidência específica e problema

- Fonte atual: `index3.html` em main `a348725a81cc0569563bed5176d5253a007bef61`, conferido com HTML público HTTP200. O rótulo é **ENTRAR GRÁTIS NO GRUPO DO WHATSAPP**, 34 caracteres incluindo espaços. A auditoria mobile de24/out documentou duas linhas em390×844/360×800, botão inteiro na dobra; a atualização da main alterou somente convites, não esse desenho.
- O canal está também explícito em `h2`: **No seu WhatsApp**, no ícone e no nome acessível **Quero entrar no grupo VIP Promos da Lidi no WhatsApp**. A redundância pode ter custo de leitura, mas também pode reforçar a clareza. Não há heatmap, pesquisa de entendimento ou dado de abandono que comprove fricção causada pelo rótulo.
- O PR#3 já tornou a ação explícita em2026-08-07. Não voltar a uma chamada genérica como “Quero receber” nem reapresentar aquele trabalho como uma hipótese inédita comprovada.

## Intervenção candidata única

| Elemento | Atual | Candidato futuro |
|---|---|---|
| Texto visível do mesmo botão | ENTRAR GRÁTIS NO GRUPO DO WHATSAPP | ENTRAR GRÁTIS NO GRUPO |

Preservar literalmente o nome acessível atual, headline/canal, ícone, geometria mínima, tipografia, cores da versão então vigente, restante da copy, scripts/Pixel/Lead/delay150ms, href/constante e recursos. Não alterar parágrafo, arquitetura da primeira dobra ou prova social no mesmo teste. Não acrescentar “sem spam”, “só administradores”, privacidade, frequência ou outra regra não confirmada.

**Hipótese:** manter ação, gratuidade e grupo, removendo a repetição visual do canal já presente, pode acelerar reconhecimento do comando e favorecer Lead/LPV. O candidato tem22caracteres: redução35,29% do comprimento, **não** aumento esperado de conversão. Não afirmar que caberá em uma linha antes de renderizá-lo; quebra de linha depende de fonte, largura e ícone. Se a única troca textual reduzir a altura natural do botão acima do mínimo existente, isso faz parte do fluxo desse rótulo; não adicionar ajustes CSS para forçar uma segunda hipótese geométrica.

**Risco principal:** retirar WhatsApp do rótulo pode reduzir clareza, especialmente para quem lê só o botão. O nome acessível preservado protege leitores de tela, mas não elimina esse risco visual. Uma palavra menor não é automaticamente melhor. O teste fica abaixo das hipóteses estruturais com evidência mais forte.

**ICE qualitativo:** impacto5/confiança4/facilidade9, não previsão de lift. Sem material adicional. Ordem atual mantida: concluir CRO-002; BL-01 se houver ofertas reais autorizadas, senão BL-02. BL-06 é alternativa específica, não autorização para executar três tratamentos.

## Gates de implementação e avaliação futura

1. Resolver o PR experimental pendente e avaliar/encerrar explicitamente CRO-002. Reconsultar main, publicação e prioridades; não criar outro PR experimental antes disso.
2. RED/GREEN para a substituição literal única dentro do CTA. Aplicar apenas essa troca ao baseline deve reproduzir o candidato inteiro byte a byte. Scripts/URLs/aria-label/controle/CSS inalterados; não “aproveitar” a edição para atualizar destino.
3. Renderizar candidato e baseline em Chromium390×844/360×800, além de320px e desktop. Conferir canal na headline, rótulo íntegro, ícone, altura mínima já vigente, foco/Enter, scroll e ausência de overflow. Capturas atuais são baseline, não QA deste candidato. Não substituir Safari real por inferência a partir da CVR de iPhone.
4. NodeVM sem rede do handler real: Lead antes da navegação/timer normal, fallbackhref, tracking ausente/erro, delay e cliques modificados preservados. Sem evento Meta real ou entrada no WhatsApp.
5. Lead/LPV principal e CPL proxy secundário; não medir sucesso pela redução de caracteres ou linhas. Congelar pré-período da versão imediatamente anterior segundo regra escolhida antes da publicação, com cobertura semanal e volume; excluir dia de publicação misto após PagesSHA+HTML.
6. MDE de planejamento proposto+3p.p., alfa5% bilateral/poder80%, amostra recalculada uma vez no baseline elegível, não reutilizar o limiar do CRO-002. Uma avaliação principal com volume/cobertura e IC95% aproximados, controle contextual e sensibilidades de mix/orçamento/dispositivo/posicionamento. Sem parada no primeiro p-valor favorável ou extensão indefinida para significância. Dados atribuídos/dependentes e campanhas distintas não permitem causalidade randomizada.

**Materiais:** os pedidos de23/out para BL-01 e comprovação de16.000/estrelas seguem pendentes; nenhuma nova cobrança nesta preparação. O fato de a prova social existir na página não a valida. Nenhum rótulo novo foi colocado na landing/PR/produção; este arquivo só prepara uma decisão futura.
