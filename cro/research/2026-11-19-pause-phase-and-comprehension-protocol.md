# 19/nov — fronteira de entrega e preparação qualitativa BL-03

## Evidência nova, não efeito da landing

MCP oficial read-only e Graph GET conciliados: 18/nov experimental192/561=34,22%, controle174/468=37,18%; 7dias12–18/nov1427/4075=35,02% versus1363/3611=37,75%. Diferença7d−2,73p.p., IC95%nominal−4,88a−0,57. Semanas05–11→12–18/nov: mudanças+0,16p.p./+1,01p.p.; diferença entre mudanças−0,84p.p., IC95%−3,80a+2,11. Não há evidência clara de evolução diferencial semanal, causalidade ou resultado do contraste ainda não publicado.

Atividades/readback confirmam pausas externas em19/nov00:08:34 e00:08:37SP nosads120250848857170505 e120252297350880505. Agora2ACTIVE/3PAUSED. Essa fronteira é posterior ao cutoff18/nov: não explica retrospectivamente esse dia nem autoriza excluir entrega histórica dos pausados. Próxima leitura19/novcompleto deve preservar o original inteiro e adicionar sensibilidade por versão criativa/ID e fase. Não resetar baseline, aguardar janela arbitrária ou atribuir mudança posterior à cor. Público/copy17/nov e controle14/nov continuam fatores externos. Responsável pela intenção operacional: ibombonato/gestor, sem recomendação de reativação automática e sem alteraçãoMeta pelo agente.

Clone separado18/nov239LPV/72Leads/R$52,65, CVR30,13%; novo conjunto136LPV versus103 do original. Não somar à primária original; comparação entre conjuntos não randomizada/50–50. Reconsulta do clone17/nov revisou gasto44,68→44,74; breakdowns atuais passam, FAIL monetário deontem permanece preservado como snapshot. Contagens atuais exatas; resíduo máximoR$0,000001. Fontes atuais: scratch2026-11-19/analysis.json,diagnostic.json,configuration-changes.json,expanded-activities.json e rawsMCP/Graph; não dados antigos substituídos.

## BL-03 — teste qualitativo de compreensão pronto, NÃO executado

**Problema observado:** a página tem CTA explícito para grupo/WhatsApp e um parágrafo de oferta, mas não há evidência direta sobre entendimento de compra, funcionamento ou obrigação percebida. FAQ própria e protótipo inline anterior geraram hipótese, não validação factual nem pesquisa com visitantes. O protótipo anterior adiciona altura/desloca benefícios: explicar mais pode também piorar atenção. Não afirmar abandono causado por dúvida sem ouvir pessoas.

**Mudança candidata objetiva:** se houver confusão demonstrada, testar um único módulo inline com a copy já delimitada no planoBL-03, usando somente funcionamento confirmado pelo responsável; não adicionar linkFAQ, scripts, novoCTA ou promessas de privacidade/admin/ausência de spam. Este roteiro refina a evidência da hipótese sem alterar o tratamento público ou oPR16. ICE qualitativo mantido **I6/C4/E8** para a hipótese de esclarecimento; confiança no lift baixa, não aumentada por criar roteiro. Se materiais/regras não forem confirmados, fallback material-free BL-02 permanece prioritário após avaliarCRO-002; entrevista não vira gate novo para contraste/layout.

### Roteiro não indutivo e registro

Aplicação futura pelo responsável com pessoas que correspondam ao público, consentimento e sem coletar telefone/nome em artefato público. Preparar exploração de compreensão, não amostra estatística de CVR. Não recrutar/postar noWhatsApp pelo agente.

1. Mostrar a mesma versão mobile atual, sem dica sobre o que deve ser entendido. Perguntar: **“O que esta página oferece, nas suas palavras?”** Registrar resposta literal anonimizada, não só avaliação do moderador.
2. **“O que você espera que aconteça ao tocar no botão?”** Codificar espontaneamente: grupoWhatsApp/conversa privada/outro/não sabe; separar tipo de destino e canal. Não perguntar “você entendeu que é grupo?” antes da resposta.
3. **“Se quisesse aproveitar uma oferta, como imagina que faria?”** Registrar expectativa de compra na loja/no grupo/outro/não sabe. Conferir regra real antes de julgar correto.
4. **“Que dúvidas ou receios fariam você não continuar?”** Resposta livre antes de opções; não sugerir spam/obrigação/fraude como primeiro estímulo.
5. Após as respostas espontâneas, quando regras estiverem confirmadas, mostrar separadamente a alternativa inline e perguntar o que mudou na compreensão. Alternar ordem em sessões diferentes quando comparar versões; ordem não randomizada é limitação.

Ficha mínima: código aleatório, data/viewport, versãoSHA, ordem de exposição, respostas literais, categoria de canal/destino/compra, dúvida espontânea, necessidade de esclarecimento e consentimento para trecho anonimizado. Não guardar contatos/prints de conversas privadas nem inventar respostas.

### Critério de uso e avaliação posterior

- Relatar contagens por categoria e exemplos reais autorizados, inclusive contradições. Não chamar percepção do moderador de taxa de conversão; não inferir prevalência populacional de poucas entrevistas.
- Se não aparecer confusão, reduzir prioridade da hipótese de copy; se aparecer, especificar a única dúvida recorrente e verificar a resposta operacional antes de escrever tratamento. Não implementar um FAQ inteiro para resolver uma dúvida.
- Quando elegível, registrar MDE/amostra próprios e baseline14dias pré-publicação pela regra escolhida antes dos resultados; primáriaLead/LPV original, CPLsecundário, controle contextual, fases de mídia explícitas. Não substituir o planoCRO002 nem reutilizar universalmente4170.
- QA de eventual módulo: inserção exata/reconstrução byteabyte do baseline, script/links/controle iguais, medir custo verticalCTA/prova/benefícios em390/360/320, screenshots e comportamento semrede. Roteiro pronto não significa teste executado, publicação, melhor compreensão demonstrada ou lift.

## Gates e pendências

CRO-002 continua único experimento Em PR16; ibombonato precisa decidir essePR. Publicação somente apósSHAdePages+HTMLconferidos; então congelar14diasanteriores, excluir dia misto e revalidar uma vez a referência4170 conforme plano. Materiais23/out e comprovação20.000/estrelas03/nov seguem pendentes, sem nova cobrança repetida. Alegação atual preservada, não endossada. Não atribuirIDnovo aoBL-03, não iniciar tratamento paralelo.
