# Auditoria de mudança visível externa e integridade da avaliação — 2026-11-03

## Entrega concreta

Identificada uma mudança real de prova social, distinta de rotação operacional: o commit humano [`b657143`](https://github.com/ibombonato/promos-da-lidi/commit/b657143cbe9cc007ff48a8d3b44a8ac98670c980), de 02/nov às18:34:25 São Paulo, alterou `index3.html` de “Mais de16.000” para “Mais de20.000”, além do convite. Deployment Pages7503989616 teve `success` às21:35:40Z/18:35:40SP. Esse horário é evidência do sistema, não instante de exposição individual. HTML atual HTTP200 idêntico àmain22751d4 confirma o novo texto; deployment7510124905/Actions41576025159 também concluídos com sucesso.

Normalizar **somente os convites** não torna o HTML experimental igual ao de01/nov. Acrescentar exatamente a substituição `16.000→20.000` torna o arquivo inteiro equivalente; CSS, headline, copy da oferta, CTA e scripts permaneceram iguais. Controle teve somente rotação externa deURLs. Portanto02/nov é dia de exposição mista àprova social;03/nov será o primeiro dia completo elegível desse novo conteúdo se não houver nova mudança. **Não há ID CRO novo nem efeito causal estimado para essa edição não planejada. CRO-001 permanece encerrado; CRO-002 não foi publicado.**

## Consequência para CRO-002 — não mudar o plano retrospectivamente

- Manter a regra pré-registrada:14dias completos anteriores àpublicação efetiva do contraste, excluindo o dia da sua publicação. Não começar novamente14dias de espera só por essa descoberta e não selecionar o baseline pelo resultado.
- No futuro congelamento, marcar a edição deprova social como mudança visível e mostrar sensibilidade por fase `até01/nov`, `02/nov misto`, `desde03/nov`; não chamar a janela inteira de tratamento visível estável.
- Se contraste for publicado antes de haver amostra suficiente na fase20.000, registrar impossibilidade de separar efeitos; não fabricar comparação homogênea, alterar evento ou declarar ganho doCTA. Preservar o agregado primário e cobertura/mix/checkpoint original.
- Na sincronização futura de#16, manter os convites e otexto humano atuais sem introduzir edição adicional. Isso **não autentica** a alegação: o guard local demonstra somente duas coresCSS versusmain. Não retornar silenciosamente para16.000 nem ampliar a prova social. Ausência de comprovação exige decisão do responsável, não invenção doagente.

## Solicitação específica ao responsável — novo dado que torna o pedido anterior desatualizado

**ibombonato:** a alegação agora é20.000. Fornecer evidência datada da contagem, grupos/fontes cobertos, definição de “recebem as ofertas”, tratamento de pessoas repetidas entre grupos, método de deduplicação e autorização para publicar. Não enviar nomes, telefones ou listas de membros; resumo agregado e comprovante anonimizado bastam. Esclarecer se as estrelas representam avaliações reais e sua fonte, ou são somente decoração. O pedido anterior de comprovação16.000 não valida20.000; este complemento é motivado por uma alteração nova, não cobrança diária dos mesmos materiais. Até resposta, considerar a prova social **não verificada**. Isso não bloqueia por si só um teste simples decontraste.

## Evidência técnica atual, sem intervenção

Chromium real390×844/360×800: capturas deprodução inspecionadas visualmente, número20.000 visível, CTA inteiro y503,75–565,75 /500,14–560,14, sem corte/sobreposição/overflow. Foto carregada, rolagem224/276px, sem exceçãoJS observada. Verde antigo ainda publicado. DomíniosMeta/WhatsApp bloqueados antes de navegar; nenhum cliqueCTA real,Lead ou entrada emgrupo. Capturas locais `baseline-390x844.png`/`baseline-360x800.png`, não screenshots deuma implementação nova. NãoSafari/WebVitals.

Guard local confirma candidato com apenasduascoresCSS. NodeVM dafonteprodução/candidato:igualdade literalhref/constantePASS,10casos comportamentaisPASS porversão,tracking ausente/erro,diferentescliques/delay150ms/Leadprénavegação,semrede.

## Gates operacionais e handoff

- #16 estáaberto,semmerge/auto-merge,headremoto`f9286a3`;GitHub retornou `mergeable_state=unknown`,não afirmar conflito nem aptidão demerge. PRoperacional#31tambémaberto,somenteURL,não outroexperimento;destino difere darota hoje publicada,conferir intenção comibombonato antes dedecisão.
- GETGitHub`/user`comacredencial designada continuaHTTP401. Nenhumaescritaremotatentada. **ibombonato/@hermes:**restaurar autenticação porcanalseguro,confirmaridentidade/permissão;depoissincronizar diário01–03/nov/atualizar#16 preservandomain. Semtokensnochat,nemdiagnósticoinventadodeexpiração.
- Diário e nota preservados emworktree/commit/patchlocal;nãoalegarPRatualizado. AponteTelegram aceitou relatório02/nov(recibo19468/hashfinalconferido);falha23/outestáresolvida. Entregadehojesóapósconclusão,distinguir deexecuçãoagendada.
