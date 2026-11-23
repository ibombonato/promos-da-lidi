# Mudança externa no targeting do clone — 2026-11-17

## Evidência nova, não experimento de landing
Graph GET de atividades registra `update_ad_set_target_spec` em **16/nov/2026 às 13:51:21 America/Sao_Paulo** no conjunto `120252642175430505` do clone `120252642171330505`. Readback por ID confirma inclusão do interesse **O Boticário (`6003358581004`)** no primeiro bloco OR de interesses, junto de Cupons e Fragrâncias. Segundo bloco, demais condições/Advantage+, idade, gênero e posicionamentos permanecem iguais no readback; não interpretar essa inclusão como condição AND adicional. O payload textual de atividade foi truncado pela API; a evidência detalhada provém do objeto atual comparado ao snapshot anterior, ambos preservados.

Campanha permanece ACTIVE/R$50/dia. União dos três IDs de anúncio sem adição/remoção: dois ACTIVE e um PAUSED como antes. Comparação POR ID encontrou somente timestamps atualizados nos anúncios; criativo, copy, destinos, tracking e status final idênticos. A ordem da lista mudou: comparação por índice produziu falsas trocas de IDs/criativo/status, preservadas como diagnóstico inicial em clone-config-delta.json, nunca adotadas como fato. `clone-semantic-delta.json` contém a comparação corrigida. Anúncios passaram por revisão após editar o conjunto, concluída por volta de13:54SP; isso não prova publicação de novo criativo.

16/nov é **dia misto do targeting do clone**. Primeiro dia completo da configuração atual:17/nov, consultável18/nov09hSP. Não reiniciar observação da campanha original, não retirar16/nov das janelas e não transformar essa transição em exigência de esperar outra janela para o contraste.

## Métricas próprias do clone
16/nov: R$58,41, 9880 impressões, 251 cliques,211LPV/66Leads proxy=31,28%, CPLR$0,885.15/nov:207LPV/81Leads=39,13%, variação−7,85p.p. São dias com exposição diferente e amostras pequenas; não demonstra efeito do interesse, canibalização ou defeito da landing. Ad120252642196110505 concentrou211LPV/66Leads/R$57,84; segundo ativo120252736506790505 teve1clique/0LPV/R$0,57, CVR indefinida (não0%). Não comparar0LPV como desempenho inferior nem supor distribuição50/50.

MCP oficial atual, diário Graph, ad-day e entrega horária conciliados exatamente. Campanhas originais foram verificadas separadamente: configuração ativa/copy/destinos/atribuição/orçamentos preservados; diferença bruta apenas miniatura assinada de anúncio antigo PAUSED. Quatro drafts idênticos, não tratados como publicados.52atividades desde14/nov paginadas, incluindo esta edição.

## Entrega concreta e plano seguinte refinado
**Handoff para ibombonato, gestor autorizado:** esta é uma nova fase de público do clone, não a publicação do CRO-002. Ao interpretar resultados, distinguir15/nov (clone original),16/nov (transição) e17/nov em diante, mantendo os totais integrais e endpoints das campanhas originais. Não é pedido de alterar orçamento/público/status nem chamado externo aberto.

BL-02 continua hipótese de compactar somente o módulo mobile (prototipagem já demonstrou CTA129px mais cedo; confiança/foto menor não avaliadas), ICEI8/C5/E8. Acrescentar ao plano preparado uma linha de proveniência por alteração externa com campanha/conjunto/ID, fuso, regra OR/AND e primeiro dia completo; vincular as sensibilidades a essa fase concreta, não a qualquer updated_time. Manter primária original Lead/LPV, clone separado, pesos de sensibilidade escolhidos antes do teste, denominadores próprios e duração inclusiva. Não somar marginais nem editar o plano/volume do CRO-002. Não implementar BL-02 enquanto#16 estiver pendente/em avaliação.

Gate atual de melhoria: decisão humana noPR#16, não falta de dados do CRO-001 ou de materiais para contraste. Pedidos de ofertas reais23/out e comprovação20.000/estrelas03/nov continuam pendentes, sem repetir cobrança ou validar alegações peloHTML. Nenhum novo ID/experimento/Meta editado.

Fontes: clone-audit.json,clone-semantic-delta.json,expanded-activities.json,mcp-clone-result.json,traffic-audit.json,today-validation.json em ~/work/hermes-scratch/cro-icb-2026-11-17/. Dados atuais, não snapshots antigos substituindo medição.
