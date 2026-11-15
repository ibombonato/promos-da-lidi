# CRO-002 — auditoria de integração sem merge e encaminhamento do bloqueio

Data: 2026-11-13. **Preparação/diagnóstico documental; não é novo experimento nem publicação.**

## Evidência nova e correção da interpretação anterior

O PR #16 continua aberto, sem merge/auto-merge, head `f9286a3666aa846deba12835c2d1fcf1d97f3d54`. Seu snapshot contém uma alegação numérica e convites antigos. Isso, isoladamente, **não prova que um merge de três vias reverteria main**. As notas anteriores pediam sincronização preventiva, mas não haviam demonstrado tal regressão.

Foi executado exclusivamente o comando de simulação local `git merge-tree --write-tree c0f29ef85bf45eb4380cdd409456b1af9c976e17 f9286a3666aa846deba12835c2d1fcf1d97f3d54`. Resultado real: exit 0, árvore `3b8f76b150eca05e80074f314123426fe15fec39`; nenhum branch/ref, worktree, PR, merge ou deploy foi atualizado. O comando pode gravar objetos Git locais, não publica nada.

Verificações byte a byte da árvore simulada:

- `index3.html` é **exatamente** o HTML da main atual com apenas `--green: #09a83a;` → `--green: #086b29;` e `--green-2: #0bc247;` → `--green-2: #087f2c;`.
- Convites atuais, alegação humana “20.000”, copy, scripts, parâmetros, recursos, CTA e rastreamento da main são preservados. Preservar a alegação não significa comprová-la.
- `index4_li.html` é idêntico ao da main. Arquivos distintos somente no allowlist do histórico, pesquisa, screenshots e experimental.
- SHA256 do candidato simulado: `3378c54b4af70a78181afbab0be325d7b6fbe8ccadcd02941ee04436c413817c`.
- Guard de escopo e Node VM sem rede: igualdade literal href/constante e dez casos comportamentais aprovados em produção e candidato. Nenhum evento real ou ingresso no WhatsApp.

**Conclusão corrigida:** não há conflito nem reversão de copy/rota demonstrados nessa integração exata. Não apresentar a idade do snapshot como regressão confirmada. Isso reduz uma incerteza técnica, mas não resolve autenticação, atualização do diário de novembro, aprovação humana ou publicação. Não equivale a nova QA visual; capturas do experimento continuam as originais do PR.

## Manutenção externa e limites desta prova

PR #38 experimental e #39 controle foram mesclados pelo humano em 12/nov. Também houve commit direto de rotação do controle. Diff desde a main anterior altera exclusivamente os dois valores de URL de cada landing, preservando tratamento visível e evento pré-redirecionamento. Pages deployment `7749322998`, sucesso em `2026-11-12T20:51:15Z`, Actions `43304285233`; ambas páginas públicas HTTP200 e byte a byte iguais ao SHA atual. CRO-002 continua com cores antigas em produção, não publicado; rotações não reiniciam Lead/LPV.

Novo PR #42 altera somente as duas URLs da experimental e permanece pendente. PR #31 também é operacional e pendente. Nenhum foi incorporado pelo agente. **Qualquer mudança de main/head invalida os SHAs desta simulação**: resolver a intenção operacional com o dono e repetir a prova sobre as refs efetivamente escolhidas, sem decidir destinos por conta própria.

## Encaminhamento executável ao responsável

**Responsável: ibombonato/@hermes.** GET autenticado `/user` retornou novamente HTTP401 `Bad credentials`; não há evidência para atribuir expiração ou revogação. Nenhum push/PATCH/POST GitHub foi tentado após esse gate.

1. Restaurar a credencial pelo mecanismo seguro existente, sem enviar tokens em chat; verificar identidade e permissão no repositório.
2. Recuperar o diário local acumulado e pesquisas de novembro pelo patch documental desta execução. Aplicá-lo na branch apropriada sem sobrescrever arquivos de landing; o patch não contém `index3.html` nem `index4_li.html`.
3. Confrontar main/head e PRs operacionais atuais; repetir `merge-tree` e os guards de escopo/CTA se qualquer ref tiver mudado. Atualizar a mesma branch do #16; não criar experimento paralelo nem force-push.
4. Ler de volta head, diff, histórico e blobs do PR; manter sem auto-merge. A decisão de aprovar/mesclar/publicar pertence ao humano.
5. Só após publicação comprovada por Pages SHA + HTML: congelar os 14 dias completos imediatamente anteriores, excluir o dia misto, revalidar uma vez a referência de volume do CRO-002 e acompanhar o plano original. Não aguardar volume adicional do CRO-001 encerrado.

## Backlog e contrato de avaliação preservados

BL-02 permanece o próximo fallback sem material (ICE I8/C5/E8), módulo de compactação mobile já prototipado; não implementá-lo com CRO-002. Acrescentar ao seu checklist de elegibilidade a prova do **resultado da integração**, não apenas do snapshot de branch, inclusive quando existir PR operacional pendente. Isso não altera a hipótese, endpoint primário CVR, regra de volume ou constitui novo gate arbitrário de dados.

BL-01 depende das ofertas reais/autorizadas solicitadas em 23/out. Comprovação agregada/datada/deduplicada de “20.000” e origem das estrelas foi complementada em 03/nov e segue sem retorno localizado; não repetir a solicitação sem novidade nem inventar prova social.

## Dados atuais: sinal de investigação, não desfecho do contraste

06–12/nov: experimental 1416/4153 LPV = 34,10%; controle 1501/4082 = 36,77%. Diferença −2,68 p.p., IC95% nominal aproximado −4,74 a −0,61. Antes, 30/out–05/nov: 36,89%/37,33%. Diferença entre mudanças −2,23 p.p., IC95% −5,05 a +0,59; diferença entre evoluções relativas −6,06 pontos percentuais. A queda não é resultado do contraste ainda não publicado. Campanhas distintas, mix, atribuição, alteração externa da alegação em 02/nov e consultas sequenciais limitam causalidade. IC nominal que exclui zero numa janela móvel não autoriza escolher um endpoint ou declarar vencedor/perdedor.

Raw/provas locais: `~/work/hermes-scratch/cro-icb-2026-11-13/merge-safety-diagnostic.json`, `summary-stats.json`, `today-validation.json`, respostas MCP/Graph, `history-read-validation.json`, `draft-comparison.json` e patch documental. Não houve mutação Meta/HTML/controle/destino, merge, auto-merge, deploy ou mensagem externa pelo agente.
