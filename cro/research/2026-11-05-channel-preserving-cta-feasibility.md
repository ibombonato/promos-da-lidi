# BL-06 — Encurtar o CTA preservando WhatsApp: benefício geométrico não confirmado

**Data:** 2026-11-05. **Estado:** pesquisa offline, sem exposição pública, novo ID CRO ou alteração de `index3.html`. CRO-002 continua Em PR #16, não publicado; CRO-001 permanece Inconclusivo no endpoint14–21/out.

## Problema e refinamento da hipótese

O candidato de28/out, `ENTRAR GRÁTIS NO GRUPO`, cabe em uma linha em390/360, mas retira o canal do comando visível. Hoje foi testada a alternativa literal **`ENTRAR GRÁTIS NO WHATSAPP`**, preservando ação, gratuidade e canal, sem adicionar promessas. A pergunta técnica era se essa alternativa também reduziria linhas/altura, não se aumentaria conversão.

**Evidência específica:** a oferta atual explica que o conteúdo é enviado “direto no grupo”, a h2 identifica WhatsApp e o nome acessível identifica grupo/WhatsApp. O CTA original de34caracteres contém todas essas informações; a alternativa de25caracteres mantém o canal, mas omite “grupo”. O destino real é convite de grupo, não conversa privada. Logo há dois riscos distintos: retirar WhatsApp do candidato anterior e retirar grupo do novo. Redundância na página ou no aria-label não demonstra compreensão de quem lê só o botão.

**Hipótese futura delimitada:** uma mensagem de ação mais curta pode reduzir esforço de leitura; a evidência de renderização deve decidir se vale testar simplificação semântica, em vez de prometer maior visibilidade. Alteração proposta, se futuramente elegível: somente o nó de texto do CTA, sem CSS, headline, geometria forçada, ícone, aria-label, tracking ou destinos. Não implementar os dois rótulos na mesma experiência.

## Comparação real, controlada apenas para pesquisa

Baseline: candidato local do CRO-002 atualizado com a main `22751d4a722a64c0640538730eeae7e1c1d393c4`; preserva convite atual e alegação20.000 **não verificada**. O verde escuro é a proposta pendente, não a versão publicada. Três arquivos derivados fora da landing do repositório: original, candidato anterior e novo candidato. A única diferença por arquivo é a linha textual do CTA; guard de reconstrução integral, CSS/scripts/href/src/aria idênticos e hash da fonte preservado.

| Viewport | Original: linhas / altura | “NO GRUPO”: linhas / altura | “NO WHATSAPP”: linhas / altura | Topo igual nas três |
|---|---:|---:|---:|---:|
|390×844|2 / 62px|1 / 56px|2 / 62px|503,75px|
|360×800|2 / 60px|1 / 56px|2 / 60px|500,14px|
|320×740|2 / 60px|2 / 60px|2 / 60px|519,97px|
|1280×900|2 / 76px|1 / 64px|1 / 64px|790,89px|

**Resultado observado:** o novo candidato **não economiza linha ou altura no mobile**, apesar de ter menos caracteres. Não adianta o topo do botão em nenhum viewport. Não diminuir fonte/padding nem esconder o ícone para fabricar esse benefício: seriam variáveis adicionais. A alternativa anterior economiza só6/4px de altura em390/360; isso não substitui a hipótese estrutural BL-02.

12combinações de variante/viewport exercitadas em Chromium real. Sem overflow horizontal, fonte e dimensões naturais preservadas, textos contidos no botão, foto e seis benefícios carregados. CTA inteiro na primeira dobra mobile. Foco Tab/Enter capturou somente a chamada local Lead e o timer150ms, com URL local inalterada; scroll nativo alcançou o fim. Sem exceçõesJS observadas. Meta/WhatsApp bloqueados antes de navegar; nenhum Lead real, entrada em grupo ou mensagem. Fonte do PR intacta. Screenshots390×844e360×800 do novo candidato inspecionados visualmente: duas linhas legíveis, sem corte/colisão. Não é Safari real, WebVitals ou teste de compreensão.

Primeiro guard local falhou por procurar a ausência de uma substring curta já contida no texto original; falha ocorreu antes de iniciar o browser. A asserção foi corrigida para comparar a linha completa e reconstruir integralmente o baseline; diagnóstico inicial preservado, não apresentado como regressão da landing ou evidência de conversão.

![BL-06 — alternativa com canal, exclusivamente offline390×844](../screenshots/research-BL-06-channel-2026-11-05-390x844.png)

[Captura offline360×800](../screenshots/research-BL-06-channel-2026-11-05-360x800.png)

## Priorização e teste planejado

**ICE mantido I5/C4/E9** para a família BL-06, sem elevar confiança de CVR por medir linhas. A alternativa com canal fica **sem vantagem geométrica mobile** e com risco de ocultar que o destino é grupo; não promovida acima de BL-02. BL-01 com material real autorizado continua prioritário quando houver insumos; BL-02 é o fallback sem material. Não introduzir CRO-003 enquanto#16 estiver pendente ou CRO-002 em avaliação.

Se BL-06 voltar a ser elegível após avaliar o tratamento atual, a decisão deve ser por **clareza**, não por “caber em uma linha”. Verificar entendimento do destino como grupo, e não conversa privada, sem induzir respostas; uma checagem qualitativa não substitui o teste de conversão. Selecionar somente um rótulo antes da implementação. Métrica principal Lead/LPV e CPL secundário; publicaçãoSHA+HTML, baseline14dias completos anteriores e dia misto excluído. Definir MDE, volume e checkpoint na elegibilidade antes de olhar o pós, com cobertura semanal, IC95% e sensibilidades por anúncio/dispositivo. Não herdar automaticamente4170LPV doCRO-002 nem fazer paradas por p-valor diário. Nenhum material opcional é gate obrigatório deste teste de texto.

## Contexto de medição e bloqueios atuais

04/nov experimental184/461=39,91%, controle191/536=35,63%; diferença+4,28p.p.,IC95%−1,76a+10,31. Recuperação diária não valida esta copy não publicada, o contraste pendente ou a alegação20.000. 7dias29/out–04/nov:37,21% versus37,26%; diferença−0,05p.p.,IC95%−1,98a+1,88. Lead é proxy pré-navegação, não participante confirmado; campanhas/eventos atribuídos não são um teste randomizado.

PR#16 continua aberto/head `f9286a3666aa846deba12835c2d1fcf1d97f3d54`, sem merge/auto-merge. GET autenticado `/user` novamenteHTTP401; nenhuma escrita remota tentada. Histórico01–05/nov e esta pesquisa são **locais até sincronização**. Responsáveis ibombonato/@hermes: restaurar autenticação segura e confirmar identidade/permissão; sincronizar o mesmo PR com main antes de decisão humana, preservando convite/copy atuais sem validar a prova social. A branch remota ainda carrega convite/alegação anteriores; não a considerar atualizada por existir um candidato local correto. Após publicação real do CRO-002, seguir sua regra original de baseline/checkpoint, sem reabrir CRO-001.

**Artefatos:** `~/work/hermes-scratch/cro-icb-2026-11-05/qa_bl06.py`, `bl06-offline/qa.json`, HTMLs/capturas offline, `initial-scope-diagnostic.json`, `daily-novelty.json`, rawsMCP/Graph e validações. Somente documentação/capturas desta pesquisa entram no commit local; nenhuma mudança de landing, controle, Meta, tracking ou destinos.
