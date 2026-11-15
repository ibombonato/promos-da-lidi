# BL-02 — separar perda entre clique e LPV da resposta ao CTA

**Data:** 2026-11-14. Pesquisa/diagnóstico, não novo experimento ou tratamento publicado.

## Evidência nova

MCP oficial read-only e série Graph atual conciliados. Comparação de semanas completas não sobrepostas: **31/out–06/nov → 07–13/nov**, no fuso America/Sao_Paulo. Queries adicionais por anúncio e dispositivo/dia reconciliam todas as datas com a série principal em impressões, cliques, LPV e Leads; gasto de breakdown pode ter resíduo de até R$0,000001. Nenhum snapshot antigo substitui respostas atuais.

| Etapa | Experimental anterior → recente | Controle anterior → recente |
|---|---|---|
| LPV / clique no link | 4675/5544 = 84,33% → 4154/5078 = 81,80% | 4777/5738 = 83,25% → 4009/4753 = 84,35% |
| Lead / LPV | 36,62% → 34,79% | 37,37% → 36,74% |

A perda experimental entre clique e LPV aumentou **2,52 p.p.**, enquanto o controle melhorou 1,09 p.p. É sinal descritivo a investigar, **não prova de lentidão, falha do navegador, abandono individual ou efeito da landing**. Os contadores atribuídos não formam uma coorte deduplicada.

### Quanto é composição de anúncios?

Decomposição simétrica com pesos de **cliques**, denominador correto desta etapa, e os quatro anúncios comuns cobrindo integralmente cliques/LPV nos dois períodos:

- Experimental: **−2,52 p.p. = −0,80 p.p. de composição −1,72 p.p. dentro dos anúncios**.
- Controle: um único anúncio; **+1,09 p.p.**, sem contribuição de composição entre anúncios.

| Anúncio experimental | Cliques/LPV anteriores | Cliques/LPV recentes | LPV/clique anterior → recente |
|---|---:|---:|---:|
| 120250848857170505 | 221/194 | 173/139 | 87,78% → 80,35% |
| 120251541120490505 | 1616/1373 | 582/492 | 84,96% → 84,54% |
| 120252297350870505 | 3473/2922 | 3472/2854 | 84,13% → 82,20% |
| 120252297350880505 | 234/186 | 851/669 | 79,49% → 78,61% |

A migração para um anúncio com taxa menor contribui, mas não explica toda a variação. “Dentro” também não identifica causa: pode incluir público, posicionamento, observação/atribuição e outros fatores.

### Dispositivo: sensibilidade marginal separada

- Android smartphone experimental: **3076/3838 = 80,15% → 2720/3561 = 76,38%**; controle **77,51% → 77,42%**.
- iPhone experimental: **1595/1702 = 93,71% → 1430/1509 = 94,76%**; controle **93,63% → 93,97%**.
- A decomposição de dispositivos comuns inclui smartphones e tablet, mas não é de campanha inteira: experimental cobre **5543/5544 cliques e 4674/4675 LPV** antes, e todos os 5078 cliques/4154 LPV depois; controle cobre **5737/5738 cliques e todos os 4777 LPV** antes, **4748/4753 cliques e 4005/4009 LPV** depois. Células excluídas e taxas não estimáveis permanecem nos raws/totais. Não imputar taxa para `other` ausente.
- Decomposições marginais de anúncio e dispositivo **não devem ser somadas** nem apresentadas como ajuste causal conjunto. O padrão não sustenta diagnosticar Safari; tampouco comprova defeito Android.

## Refinamento específico da hipótese seguinte

**BL-02 permanece:** compactar somente o módulo mobile para antecipar oferta/CTA, preservando texto, recursos, botões, rastreamento e destinos. **ICE I8/C5/E8**, sem elevar confiança pela nova associação e sem prometer melhoria de velocidade. O protótipo offline anterior mostrou avanço geométrico de129px, não CVR ou Web Vitals.

**Novo guard do plano:** acompanhar separadamente (1) LPV/clique, por anúncio e dispositivo com cobertura explícita, e (2) Lead/LPV, desfecho principal. Congelar os pesos de cada denominador em seu próprio pré-período; não usar pesos de LPV para explicar LPV/clique. Se a aquisição mudar durante o teste, preservar o resultado principal e reportar essa limitação, sem apagar dias, mudar tracking ou declarar que a compactação corrigiu carregamento. CPL continua secundário; não promover uma métrica favorável a novo endpoint.

Antes de propor otimização de carregamento, seriam necessárias medidas reais de recursos/tempos em ambiente controlado e, para conclusões de campo, dados de campo disponíveis/autorizados. Essa pesquisa **não torna tal coleta pré-requisito para CRO-002 ou BL-02**. Não reduzir imagem, adicionar biblioteca ou mudar Pixel sob a hipótese de contraste/arquitetura.

## Estado e ação humana

CRO-002 continua **Em PR #16, não publicado**. Não executar BL-02 em paralelo. CRO-001 encerrado Inconclusivo não reaberto. GitHub GET `/user` com credencial existente retornou **401 Bad credentials**, gh sem login; nenhuma escrita remota tentada. **ibombonato/@hermes:** restaurar autenticação segura/identidade/permissão e sincronizar diário preservado; ibombonato decidir #16. Sem essa decisão não há volume pós-CRO-002 a aguardar.

Main `e58525718798b40031e2cb18974f50ccb64cfdf1`, Pages deployment7781105426 success em14/nov02:14:24Z e Actions43545103765 success; ambas landings HTTP200 idênticas à main. #42 e #44 rotacionaram somente convites por ação externa, sem reset de baseline. #45 pendente também contém só URLs; não foi incorporado. Simulação três-vias main+#16 produziu árvore `45de49b184060559ed2804c2f90cde9a617d43cf`, index3 exatamente main+duascores e controle idêntico. Não é merge/publicação e exige revalidação se main/head mudar. Alegação20.000/estrelas continua sem comprovação independente; não foi endossada.

## Evidência e limites

Artefatos atuais: `~/work/hermes-scratch/cro-icb-2026-11-14/` — `lpv-link-diagnostic.json`, quatro `lpv-link-*-raw.json`, `analysis.json`, `today-validation.json`, MCP/Graph atuais, drafts, Pages/live, merge-tree e NodeVM. A identidade da decomposição foi testada sem arredondar; a lista de anúncios e datas foi reconciliada. Não houve implementação ou nova captura mobile nesta análise; screenshots do PR são os originais, não teste Safari ou performance de campo. Nenhum evento Meta real, entrada em grupo, mensagem, merge, deploy ou alteração Meta/HTML/destinos.
