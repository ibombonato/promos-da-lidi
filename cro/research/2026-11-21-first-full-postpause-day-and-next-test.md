# 21/nov — primeiro dia civil inteiramente após as pausas

Fonte atual: 2026-11-21T12:03:13.420917+00:00; 145 conciliações PASS, janelas MCP/Graph1/3/7/14 exatas. Contagens de breakdown exatas; resíduos monetários estritamente subcentavo. Lead é proxy de clique, não participante confirmado.

## Entrega concreta: avaliação da hipótese operacional de melhora após realocação

As pausas externas ocorreram em19/nov00:08:34/37SP.19 ainda é misto;20 é o primeiro dia civil integral posterior. Nenhuma pausa/edição feita pelo agente. A hipótese diagnóstica de que a retirada de anúncios elevaria imediatamente a CVR não se confirmou de forma consistente; não é um experimento randomizado nem justificativa para reativar anúncios.

| AdID sobrevivente | LPV19→20 | Leads19→20 | CVR19→20 |
|---|---:|---:|---:|
| 120251541120490505 | 95→84 | 36→36 | 37,89%→42,86% |
| 120252297350870505 | 493→390 | 176→125 | 35,70%→32,05% |

Agregado dos mesmos IDs19→20: 212/588=36,05% → 161/474=33,97%; Δ-2,09p.p., IC95%nominal[-7,85; 3,68]. Composição0,10p.p. + dentro dos anúncios-2,19p.p. = mudança total. Aritmética marginal, não causa; mesmoID não fixa público/creative/alocação. Par pausado sem entrega reportada20/nov; suas contribuições históricas anteriores continuam no principal.

## Decisão e handoff ao responsável

CRO-002 permanece EmPR#16, não publicado. HTML de ambas as páginas igual ao SHA127eb14fd0d31364d4519a6143472310ed927e72; deployment7956709874success2026-11-21T01:42:30Z/Actions44851693166success. ibombonato: decidir o teste de contraste já preparado; não há volumeCRO001 pendente. Não mudar Meta por estes números. Se a decisão for não testar contraste, registrar disposição humana explícita antes de avançarBL-02, sem abandono silencioso/PRparalelo.

## Refinamento do próximo teste — BL-02, não implementação

Problema: oferta/CTA ocupam a região inferior da dobra, enquanto o módulo superior consome248px; protótipo já auditado antecipou129px sem mudar oferta. Alteração única futura: compactação do módulo mobile, preservando headline/CTA/cores então aprovadas/scripts/destinos. ICEI8/C5/E8, sem confiança adicional emlift. Evidência nova de20/nov demonstra por que a análise futura não pode usar a primeira recuperação após pausas como baseline escolhido pelo resultado.

Plano: publicar somente depois de avaliar/fecharCRO002; congelar14dias completos anteriores pela regra temporal, não porstatus atual; dia de publicação excluído. CVR agregado original primário; CPL secundário; clone e sensibilidades porfase/IDs/pesos congelados separados. Comparação pré-especificada de todosdiassemana comuns, sem selecionar dias favoráveis. MDE/volume próprio será calculado com baseline real quando elegível. Não redefinir4170doCRO002. QA390/360/desktopbaixo/texto ampliado permanece gate da eventual implementação. Sem necessidade de novos materiais paraBL02; pedidos deofertas e comprovação20.000/estrelas seguem pendentes, não reiterados hoje.


**Nova atividade a esclarecer com gestor ibombonato:** first_delivery_event de20/nov19:08:36SP para ID120252802586720505, associado no extra_data ao conjunto clone120252802517710505. ID ausente da lista configurada; GET explícito retornouHTTP400/code100/subcode33 (inexistente, sem permissão ou operação não suportada, sem distinguir causa). Não inventar anúncio/criativo/destino/status, nem chamar de nova exposição identificada ou gasto oculto. Todas as contribuições ad-day retornadas conciliam exatamente a campanha; hierarchy atual semanticamente igual não resolve a identidade desse evento. Gestor deve confrontar o ID no histórico do AdsManager; sem ediçãoMeta pelo agente. Evidência emnew-first-delivery-object.json/expanded-activities.json.
