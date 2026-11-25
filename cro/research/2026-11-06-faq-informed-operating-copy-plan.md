# BL-03 — Explicar a compra sem desviar o funil ICB

**Data:** 2026-11-06. Entrega documental de backlog; não é CRO-003, implementação, renderização de candidato ou resultado de conversão. CRO-002 permanece o único experimento em PR (#16); CRO-001 continua encerrado Inconclusivo.

## Evidência nova verificada

Os PRs humanos #32 e #33 publicaram uma FAQ independente, `https://www.lidimelo.com.br/faq.html`. Deployment Pages `7592311961` success em 2026-11-06T04:23:54Z e Actions `42162192857` success para `21c6f1d608c0a9aac84edb83402c28742a53acad`. GET público da FAQ HTTP200, byte a byte igual ao commit; SHA256 `a896d5b9985e939ced9aab7021f0789230641c890642ec1764744494e7861d93`.

- A FAQ contém 12 perguntas. Em `#quem-vende-e-entrega`, o texto publicado diz: “Eu indico a oferta e o cupom; o pedido é feito por você, direto no site oficial da loja.”
- Em `#produto-que-nao-enviei`, aparece “no grupo só eu envio mensagens”. Isso é uma declaração de primeira parte publicada pelo responsável, **não inspeção independente das permissões de todos os grupos**. Não transformar em promessa universal de administração, frequência, privacidade ou ausência de spam.
- `index3.html` e `index4_li.html` são byte a byte iguais ao snapshot de ontem. Não existe link para `faq.html` em `index3.html`; a publicação da página independente não constitui alteração do tratamento ICB nem início de experimento.
- Auditoria é de fonte/GET, não visual ou teste funcional da FAQ. Nenhum CTA foi acionado ou evento enviado.

## Separação técnica obrigatória

A FAQ tem Pixel `1007235838588459`, evento `FAQGrupoClick` e sorteio entre dois convites. A ICB experimental mantém Pixel `1504398471438133`, evento `Lead`, convite único e handler original.

Logo, **não adicionar um link para essa FAQ como atalho para tratar objeções na ICB**: ele poderia desviar o visitante para outro roteamento/evento. Isso alteraria o funil e não está autorizado. Diferença de Pixel é configuração da página independente, não defeito comprovado da ICB. Não copiar scripts, convites, eventos, links comerciais, telefone de suporte ou a imagem de resgate para a experimental. Não modificar a FAQ — arquivo fora do escopo CRO.

## Hipótese refinada e intervenção delimitada

**Problema possível:** a landing diz que recebe ofertas, mas pode deixar dúvidas sobre o que acontece se a pessoa quiser comprar ou se o botão já inicia atendimento/pedido. Não há pesquisa com usuários ou taxa de dúvidas que quantifique esse obstáculo. A FAQ oferece uma nova fonte de linguagem de primeira parte, não prova de abandono.

**Candidato textual para um único módulo inline, após o CTA existente e antes da prova social:**

> **Como funciona a compra?**  
> Você recebe ofertas e cupons no grupo. Se quiser comprar, abre o link da oferta e faz o pedido na loja.

Explicação proposta, ainda não implementada. Sem accordion, link secundário, novo botão ou novo evento. Manter headline, oferta, rótulo/cores do CTA da versão então aprovada, fotografia, prova social, benefícios, todos os href/src, Pixel e scripts. O resultado avaliaria a inclusão desse módulo, não cada frase separadamente. Nada de “sem spam”, número oculto, entrada imediata, aprovação dispensada, frete garantido, cupons sempre válidos ou suporte personalizado.

**Justificativa/comportamento esperado:** reduzir a incerteza sobre indicação versus venda e sobre a etapa de compra, sem tirar o visitante da landing ou prometer regras não verificadas. **Risco:** introduzir compra cedo demais pode elevar a percepção de compromisso ou aumentar leitura/deslocar argumentos posteriores; não supor benefício só porque o texto é explicativo.

**ICE qualitativo:** impacto6 / confiança5 / facilidade8. Confiança na hipótese de CVR continua moderada; a FAQ não aumenta a confiança estatística. Prioridade permanece abaixo de BL-01 com exemplos reais e BL-02 sem materiais; não promover automaticamente por existir uma página nova. BL-06 conserva seus riscos de clareza de canal/grupo.

## Plano do futuro teste — não altera CRO-002

1. Só tornar experimento depois de decisão/publicação/avaliação explícita do CRO-002 e ausência de outro PR experimental pendente. Hoje não atribuir novo ID e não criar PR paralelo.
2. Revalidar fidelidade da frase à operação e à oferta vigente antes da implementação. Não precisa de depoimentos, ofertas ilustradas nem prova do número20.000 para testar essa explicação; alegações administrativas seguem fora do candidato.
3. Escolher e registrar antes do pós a referência da versão imediatamente anterior, MDE planejado, volume e cobertura semanal; calcular amostra com os LPV/Leads efetivos nessa ocasião. Não congelar hoje um baseline futuro nem herdar automaticamente4170 do CRO-002.
4. Principal Lead/LPV, secundária CPL proxy; Wilson95% e incerteza da diferença antes/depois, controle contextual e sensibilidades pré-especificadas por anúncios/dispositivo/posicionamento. Não usar leitura do módulo ou evento FAQGrupoClick como conversão. Campanhas distintas/eventos atribuídos não são coortes randomizadas ou participantes confirmados.
5. QA RED/GREEN de inclusão única do módulo; scripts/CSS já existente/href/src/controle preservados. Chromium390×844 e360×800, fallback320, desktop baixo, texto ampliado/teclado/reduced-motion; medir altura do módulo, CTA e exposição da prova social/benefícios. Sem inferir geometria pelo comprimento do texto. NodeVM do CTA real sem rede; Meta e WhatsApp bloqueados antes da navegação. Screenshots só serão de implementação quando essa etapa de fato ocorrer.
6. No checkpoint pré-registrado, avaliar explicitamente; fechar Inconclusivo quando adequado, sem prolongar só para significância. Reversão só em PR para aprovação humana.

## Gates e encaminhamento de hoje

- GitHub GET `/user` com a credencial salva continua HTTP401. Nenhuma escrita remota tentada. **ibombonato/@hermes:** restaurar autenticação segura e confirmar identidade/permissão; depois sincronizar o mesmo PR#16 com main, preservando o convite e a alegação humana atual sem endossá-la. A branch remota ainda contém16.000/convite anterior. Não aprovar essa versão desatualizada como se estivesse sincronizada.
- Após sincronização, ibombonato decidir #16. Só depois de publicação confirmada por SHA+HTML congelar14dias pré-publicação/excluir dia misto e revalidar uma vez a referência4170 pelo plano do CRO-002. Não falta volume do CRO-001 nem material opcional para o contraste.
- Pedidos reais23/out e comprovação agregada/datada/deduplicada20.000/estrelas complementada03/nov continuam pendentes; não houve nova resposta nas fontes consultadas ou nova cobrança hoje.

**Artefatos atuais:** `~/work/hermes-scratch/cro-icb-2026-11-06/daily-novelty.json`, `live-faq.html`, respostas de PRs/deployments/Actions e `today-validation.json`. Nenhuma mutação Meta, merge, auto-merge, deploy, alteração de landing/FAQ/rastreamento/destino ou mensagem externa pelo agente.
