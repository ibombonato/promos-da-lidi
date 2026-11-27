# BL-02 — Sensibilidade por dia da semana e proteção contra falso lift

**Data:** 2026-11-11. Pesquisa e planejamento, não experimento implementado; nenhum novo ID CRO. CRO-002 continua Em PR #16, não publicado. Toda esta nota permanece LOCAL enquanto GitHub retorna HTTP401 no GET /user.

## Evidência nova, coletada hoje

Série Graph GET por anúncio/dia de **03–10/nov**, conciliada exatamente com cada campanha/dia em investimento, impressões, cliques, LPV e Leads; respostas brutas preservadas. Ambas as terças já usam a alegação externa20.000, cuja veracidade continua não comprovada. Não escolher estes dois dias como novo endpoint: são uma sensibilidade de calendário e composição.

| Terça-feira | Experimental LPV/Lead/CVR | Controle LPV/Lead/CVR |
|---|---|---|
| 03/nov | 848 / 268 / 31,60% | 795 / 276 / 34,72% |
| 10/nov | 569 / 203 / 35,68% | 562 / 185 / 32,92% |

A experimental variou **+4,07p.p.**, o controle **−1,80p.p.**; diferença entre mudanças **+5,87p.p., IC95% nominal aproximado−1,29a+13,04**. São dois dias, eventos atribuídos/potencialmente dependentes e campanhas distintas, sem randomização. Não demonstram efeito da landing ou vitória do CTA ainda não publicado. A comparação semanal completa28/out–03/nov→04–10/nov tem diferença entre mudanças **−0,16p.p., IC95%−2,99a+2,67**. O contraste entre diagnósticos impede tratar a terça favorável como resultado principal.

Na experimental, decomposição simétrica da variação+4,07p.p. = **−1,70p.p. de composição +5,77p.p. dentro dos anúncios**, identidade reconciliada antes de arredondar. Os anúncios lançados21/out passam de548/848LPV para489/569LPV (**64,62%→85,94%**); isso não explica aritmeticamente toda a recuperação. Padronizando a terça10/nov pelos pesos dos anúncios de03/nov, CVR=**36,11%**, contra35,68% agregada. As menores células têm16/15LPV; padronização é instável e não ajusta causas internas ou a combinação anúncio×dispositivo. Não somar decomposições marginais nem declarar que novos anúncios venceram.

## Refinamento concreto do próximo teste BL-02

- **Problema:** resultado agregado pode variar com distribuição/dia da semana; não basta uma terça favorável para concluir que compactação funcionou.
- **Mudança objetiva futura:** somente compactar o módulo mobile da primeira dobra conforme protótipo width-only existente, preservando headline, oferta, rótulo/handler/links/Pixel e contraste da versão então aprovada. Não adicionar explicação inline ou trocar CTA simultaneamente.
- **Justificativa/impacto esperado:** antecipar oferta/CTA e exposição dos benefícios, não prometer lift nem usar recuperação sem alteração como validação.
- **ICE:** I8/C5/E8 mantido; confiança não aumentada por dados observacionais.
- **Plano acrescentado antes da implementação:** preservar primária cumulativa e checkpoint próprios; congelar uma vez pesos dos anúncios no pré-período; apresentar cobertura por dia da semana e por anúncio nos períodos inteiros. Acrescentar sensibilidade de calendário usando TODOS os dias da semana comuns, não escolher retrospectivamente apenas o melhor par. Células sem LPV ficam não estimáveis, sem taxa imputada; IDs novos/removidos e tráfego excluído serão explicitados. Mantém-se a comparação agregada mesmo se padronização alterar o sinal. Isso NÃO muda plano/baseline/4170LPV do CRO-002 nem cria espera por outra janela limpa.
- **Gates:** decidir/sincronizar o experimento pendente e avaliar explicitamente seu resultado antes de iniciar BL-02; zoom real/texto ampliado e investigação da diferença de foto no desktop permanecem QA antes de futura implementação. Ofertas/depoimentos opcionais não bloqueiam compactação ou contraste.

## Reconsulta de exposição e pendências

O clone120252642171330505, seu conjunto e anúncio continuam PAUSED; Graph09–10/nov retorna data[] (nenhuma linha reportada, não null convertido em zero). Destino efetivo não foi reconfirmado com permissão de post, e continua não confirmado; não derivar do nome. Não entra nos totais das duas campanhas medidas.

A consulta MCP de métricas hoje não ofereceu next_actions; uma consulta explícita read-onlyobject_state=draft na mesma sessão/conversa encontrou os mesmos **quatro rascunhos**, IDs/time_updated/status/valores novos intactos. A única diferença de payload foi omissão do contexto `old`, não publicação/apagamento. Configuração live das duas campanhas alvo, ativos e conjuntos permanece semanticamente igual; só a miniatura assinada do antigo pausado rotacionou. O gestor deve continuar conferindo pendências versus live antes de eventual publicação manual em lote, sem ação Meta pelo agente.

## Bloqueio que realmente impede avançar o teste

**ibombonato/@hermes:** restaurar a autenticação GitHub por canal seguro, validar GET/user e permissão de escrita no repositório, sincronizar o mesmo PR#16 com main e o histórico local01–11/nov e só então decidir o contraste. O readback público continua aberto/headf9286a3/semmerge/auto-merge, mas a branch remota está desatualizada em convite/16.000; não aprová-la como atual. Nenhuma escrita remota foi tentada apósHTTP401, nenhuma causa de expiração/revogação inventada. Não falta amostra do CRO-001, nem material para contraste; não abrir outro experimento para contornar o gate.

Pedidos de ofertas reais23/out e comprovação agregada/datada/deduplicada de20.000/estrelas03/nov permanecem pendentes; sem nova cobrança repetitiva ou uso como evidência validada.

**Proveniência:** `~/work/hermes-scratch/cro-icb-2026-11-11/`: weekday-ad-day-*-raw.json, weekday-diagnostic.json, contribution-validation.json, mcp-explicit-drafts-result.json, draft-response-differences.json, clone-current.json, analysis.json, today-validation.json. Nota exclusivamente documental; landings/Meta/destinos/rastreamento intactos, sem merge/deploy/novo evento real ou entrada WhatsApp.
