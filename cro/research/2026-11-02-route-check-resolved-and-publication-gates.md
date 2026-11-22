# Resolução da ressalva literal de rota e gate de publicação — 2026-11-02

**Estado:** auditoria/documentação, não novo experimento. CRO-002 permanece Em PR #16, não publicado; CRO-001 continua encerrado Inconclusivo. Sincronização desta nota e dos diários de 01/02-nov ainda **LOCAL**, bloqueada por HTTP401 no GitHub.

## Entrega concreta

O responsável integrou o PR operacional #30 em 01/nov15:43:58Z. O diff `3df84c5..6156056` de `index3.html` muda exclusivamente as duas URLs de convite; nenhuma alteração no controle. A nova fonte já deixa href e constante exatamente iguais, sem query. **A falha literal documentada em26/out deixou de ocorrer na produção atual** por manutenção externa, não por correção não autorizada do agente. Não inferir retroativamente o significado dos parâmetros anteriores.

- Publicação confirmada: SHA `615605697d2dc6c481094f991591680040649808`, deployment7475240488 success01/nov15:44:37Z, Actions41322703411 success, ambas landings públicas HTTP200/byte a byte iguais àmain.
- Após mascarar somente convites, HTML inteiro idêntico à versão anterior: headline, CTA visível, CSS, Pixel, Lead e handler preservados. **Não reiniciar baseline Lead/LPV.** O clique é registrado antes do redirecionamento, não confirma entrada no grupo.
- Worktree de hoje incorporou main atual preservando o histórico pendente/diário local de01/nov. Guard da proposta confirma somente duas cores CSS contra main; controle/scripts/copy/URLs iguais àmain.
- Script real em Node VM, sem rede: **10 casos comportamentais PASS e igualdade literal href/constante PASS**, emprodução eproposta; tracking presente/ausente/comerro, delay150ms, modificadores/central/direito/eventocancelado. Zero eventosMeta/entradasWhatsApp. Sem novo tratamento visual, não alegar nova QA mobile/Safari ou capacidade do grupo.

## Dois gates restantes, com responsáveis

1. **ibombonato/@hermes — autenticação:** GET GitHub `/user` com a credencial já designada ao helper retorna HTTP401/`Bad credentials`, novamente. Causa não estabelecida; não afirmar expiração/revogação. Restaurar credencial pelo canal seguro e verificar identidade/permissão no repositório antes dequalquer push. Não houve tentativa deescrita remota apósofail. Histórico preservado emcommit/patch local; não alegar atualização doPR.
2. **ibombonato — decisão do único experimento pendente:** #16aberto/semmerge/auto-merge, sem comentários/reviews. Após aprovação humana e publicação realmente confirmada, congelar14dias completos imediatamente anteriores/excluir dia misto erevalidar uma vez a referência4170 conforme plano. Não falta volume deCRO-001 nem material paraocontraste; não iniciarBL-02 emparalelo.

## Qualidade da medição e entrega

MCPoficial retornou code4/subcode1504022 `Too many API requests` transitório na primeira consulta7d; retry posterior concluiu sem alterar Meta. Na própria execução, impressão experimental01/nov revisou21738→21739: guard exato interrompeu aconciliação, primeiro snapshot arquivado, MCP1/3/7/14d+série diária/breakdowns reconsultados. Totais finais, leituraGraphdelivery-only ehorária agora **exatos**, sem tolerar divergências de contagem ou reutilizar números antigos. LPV/Leads/gasto inalterados; nenhuma revisão dos dias comuns com snapshotde01/nov.

Quarta jornada completa desde retomada29/out:01/nov594LPV/R$156,48;29/out–01/nov2709LPV/1047Leads,38,65%. Há continuidade observada em quatro dias, não causa28/out esclarecida ou recuperação definitiva; preservar incidente nasjanelas e encaminhamento do gestor para AdsManager/suporte se recorrência. Novos anúncios hoje346LPV/142Leads=58,25%dosLPV; não atribuir CVR41,08% àcor ainda não publicada nem ao mix sem isolamento.

Execução01/novcompleted e reciboTelegram19420 conferidos porhandle/ID/hash daresposta final extraída. Falha antiga23/out não é estado atual. Entrega dehoje depende da conclusão posterior; nenhum envio direto/reconfiguração/agendaalterada.
