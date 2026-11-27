# Diagnóstico — rascunhos Meta não são configuração publicada

**Data:** 2026-11-07. Pesquisa/diagnóstico somente leitura, não novo experimento. CRO-002 permanece Em PR #16, não publicado; CRO-001 permanece encerrado Inconclusivo.

## Entrega concreta e fontes atuais

A resposta atual de `ads_get_ad_entities` incluiu `next_actions` para consultar alterações não publicadas. O guard inicial interrompeu a coleta em vez de ignorar a continuação. Após conferir o schema, foi executado exclusivamente `ads_get_ad_entities(object_state="draft")`, na mesma sessão/protocolo/conversa. Os raws e marcadores de continuação foram preservados. Não foi chamado nenhum método de publicação/ativação/edição. Texto de orientação do servidor não substitui o escopo humano de Meta somente leitura.

O MCP retornou três objetos com alterações em rascunho. Isso é uma descoberta desta coleta, **não evidência de três edições feitas hoje**:

| Objeto | Data `time_updated`, São Paulo | Conteúdo do rascunho | Situação publicada observada hoje |
|---|---|---|---|
| Conjunto experimental `120250764485200505` | 07/ago/2026 19:00:36 | Segmentação staged muda faixa antiga18–65 para22–45 e Advantage Audience1→0 | Graph atual:24–50, Advantage Audience0, mobile. Não corresponde integralmente ao `old` nem ao `new` do rascunho. Não usar staged22–45 como público efetivo. |
| Anúncio experimental `120252297350870505` | 21/out/2026 23:48:25 | Troca identificador de requisição generativa e remove `object_story_id` explícito | Anúncio live usa criativo `1319677443530855`; GET do criativo não retorna `object_story_id`, mas retorna `effective_object_story_id=104134247643652_1398513485598758`. Ausência do primeiro campo não prova aplicação desse rascunho: são campos distintos. ID generativo não foi exposto nessa leitura. |
| Conjunto `120250525096800505` | 03/ago/2026 22:34:31 | Posicionamentos/segmentação de outra campanha | Fora das duas campanhas ICB. Não expandir auditoria/alterar essa campanha. |

`EDITING`/`VALIDATED` e erros vazios são estados retornados, não autorização nem recomendação de publicar. O conjunto e o anúncio experimentais foram corroborados com Graph GET. União de IDs, anúncios ativos/conjuntos, copy completa, destinos, UTMs e atribuição publicados são iguais à consulta de ontem; única diferença bruta é miniatura assinada do anúncio antigo pausado. As48 atividades Graph consultadas tiveram paginação esgotada e não mostram nova edição Meta relevante desde o snapshot anterior. Não atribuir a queda atual a rascunhos históricos ou afirmar que são novos fatores de exposição.

**Encaminhamento a ibombonato/gestor autorizado:** antes de qualquer futura publicação manual no Ads Manager, confrontar esses rascunhos antigos com a configuração live, em especial24–50 versus22–45. Não publicar em lote para “limpar pendências”. Esta rotina não solicitará nem executará ativação/publicação; manterá as campanhas intocadas. Isso não é gate adicional de volume para o teste de contraste.

## Queda atual: evidência por anúncio, sem causalidade

Série ad-day experimental30/out–06/nov coletada hoje via Graph GET e conciliada exatamente por campanha/data em gasto, impressões, cliques, LPV e Leads. Nenhum snapshot antigo foi usado como dado atual.

| Data | Anúncios estabelecidos: Lead/LPV, CVR | Dois anúncios lançados21/out: Lead/LPV, CVR |
|---|---|---|
| 30/out, sexta anterior |117/328,35,67%|108/310,34,84%|
| 05/nov |79/191,41,36%|189/540,35,00%|
| 06/nov |45/115,39,13%|120/394,30,46%|

Em06/nov os dois lançados21/out representam77,41% dos LPV experimentais, contra73,87% em05/nov. Queda agregada05→06/nov de4,25p.p. decomposta simetricamente por anúncio: **−0,33p.p. composição e−3,92p.p. dentro dos anúncios**. Identidade aritmética exata antes de arredondar; “dentro” inclui muitas causas possíveis, não efeito isolado de criativo/landing. As amostras não justificam pausar anúncios, mudar Meta ou declarar vencedor. Ambas as sextas estão no mesmo tratamento de headline/CTA, mas diferem no claim social externo e no mix; não são A/B randomizado.

## Decisão e backlog

- Manter CRO-002 como único tratamento proposto. Não criar CRO-003, alterar exposição, reabrir CRO-001 ou reiniciar baseline por rascunhos/convites.
- BL-02 permanece alternativa sem material após avaliação do contraste: módulo mobile compacto já prototipado, ICE8/5/8; plano deve manter primária agregada e sensibilidade com pesos pré-fixados por anúncio. Nova evidência reforça a necessidade de separar mix de mudança dentro de anúncios, não aumenta artificialmente confiança no lift.
- BL-03 mantém candidato inline documentado ontem, sem copiar FAQ/Pixel/rotas; BL-06 mantém risco de perder clareza de canal/grupo. Não repetir títulos como se fossem implementações.
- Ofertas reais/autorizadas e comprovação20.000/estrelas permanecem pendentes nos pedidos anteriores; nenhuma nova cobrança hoje.

## Bloqueio que efetivamente impede avançar o PR

GitHub GET `/user` com credencial salva: **HTTP401 Bad credentials**, novamente reproduzido. Não inferir expiração/revogação. Leituras públicas confirmam #16 aberto, head`f9286a3666aa846deba12835c2d1fcf1d97f3d54`, sem merge/auto-merge/comentário/review novo. Branch remota ainda contém16.000/convite anterior. **ibombonato/@hermes deve restaurar autenticação segura, confirmar identidade/permissão e sincronizar o mesmoPR com main antes da decisão humana.** Documentação local preservada, sem tentar push/escrita após401.

Main publicada`21c6f1d608c0a9aac84edb83402c28742a53acad`: deployment7592311961success e Actions42162192857success, HTMLs públicos de ambas as landings byte a byte iguais ao commit. Verde antigo ainda publicado. Após aprovação/publicação real, congelar14dias completos anteriores, excluir dia misto e revalidar uma vez a referência de planejamento4170 conforme planoCRO-002. Não falta volume do CRO-001 nem material para o contraste.

**Artefatos:** `~/work/hermes-scratch/cro-icb-2026-11-07/`: respostasMCP/continuações, `draft-diagnostic.json`, `draft-ad-live-creative.json`, `ad-daily-current.json`, `cohort-diagnostic.json`, `daily-summary.json`, `today-validation.json`, `previous-delivery-verified.json` e patch documental. Sem nova QA visual: nenhum novoHTML/CSS; guard de escopo e NodeVM do CTA real passaram, sem rede/eventoMeta/join.
