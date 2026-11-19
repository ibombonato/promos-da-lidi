# 01/nov/2026 — bloqueio GitHub e diagnóstico da retomada

## Entrega concreta e responsáveis

1. **Bloqueio novo reproduzido:** autenticação GitHub disponível ao helper retorna HTTP401 `Bad credentials` também no GET `/user`. `gh auth status` não encontrou login. A leitura pública dePRs/commits/Actions/deployments e o fetch Git continuaram funcionando. Isso não demonstra permissão de escrita. Nenhum push/PATCH/criação dePR foi tentado após a falha. Não concluir que o token expirou, foi revogado ou perdeu escopo: a causa precisa ser verificada pelo titular.
2. **ibombonato / operador @hermes:** restaurar a credencial GitHub deste ambiente pelo armazenamento seguro, sem enviar token no chat nem copiar credenciais de outro perfil; verificar identidade e permissão do repositório. Depois publicar apenas os dois arquivos documentais desta rodada na branch já vinculada aoPR#16, por fast-forward e com readback. Branch local `docs/cro002-monitor-2026-11-01`; atualização remota **pendente**. A credencial Meta segue válida e foi usada só para leitura.
3. **Decisão humana separada:** CRO-002 continua EmPR no#16; ibombonato decide o experimento e oPRoperacional#30. Não incorporar antecipadamente o convite do#30. Após eventual aprovação, confirmar publicaçãoPages+HTML antes de congelar baseline/medir o tratamento. Não criar experimento paralelo.

## Evidência de entrega e iPhone

MCPoficial eGraphGET atuais reconciliados nas quatro janelas; Graphdelivery-only/horário conciliam exatamente o dia31/out. Experimental: 766LPV,302Leads proxy,R$210,38,27891impressões,879cliques. Terceiro dia completo de entrega retomada (29–31/out), não comprovação de causa resolvida para28/out. Orçamento nominalR$150 preservado; gasto equivale a140,25% dele, não prova de edição. Conta/hierarquia permanecem ativas e sem erro exposto; investigação de avisos/limites/cobrança da interrupção continua com gestor autorizado, suporte se recorrência. Manter28/out no histórico, sem seleção de dias favoráveis.

O sinal iPhone de30/out não persistiu com a mesma magnitude: experimental58/217=26,73%→86/263=32,70% em31/out; controle90/246=36,59%→95/252=37,70%. Androidexperimental216/502=43,03% em31/out. Dispositivo não identifica navegador; não comprova defeitoSafari, efeito de CSS ou mudança de qualidade. Reconsulta29–31/out com dados brutos em `ad-device-daily-raw.json`, contagens exatas e resíduo monetário máximoR$0,000001 nos breakdowns.

Novos anúncios em31/out: 437LPV/160Leads,57,05%dosLPV. Decomposição simétrica30→31/out: CVR+4,16p.p. = -0,35p.p.composição + 4,51p.p.dentro dos anúncios. Identidade aritmética reconciliada antes de arredondar, não atribuição causal nem teste igualitário decriativos.

## Integridade e observações seguintes

CRO-001 permanece Inconclusivo no endpoint14–21/out, sem reabertura. CRO-002 não foi publicado; não chamar os resultados acima de efeito do contraste. BL-02 segue o próximo teste sem material após avaliação explícita doCRO-002 (ICEI8/C5/E8); protótipooffline31/out já existe e ainda requer desktopbaixo/zoom/reduced-motion antes da implementação. MaterialBL-01/provasocial pendente do pedido23/out, sem cobrança repetida.

Publicação atual: deployment7443782385success/Actions41092320136success para3df84c5ede7eda8e73d6c167ef4f0e8644eea460, com ambas páginas públicasHTTP200 idênticas aessecommit. EndpointPagesbuild sem autenticação retornou404; prova alternativa usou deployment eActions públicos mais HTML, não inferência de publicação por merge. PR#30 inspecionado integralmente: somente duas referências de convite, sem alteração do tratamento. Não implementado pelo agente. GuardCRO-002PASS: apenasduascoresCSS; controles/scripts/URLs intactos. NodeVMsemrede10casoscomportamentaisPASS; igualdade literalhref/constanteFAIL conhecida porqueryexterna preservada. NenhumQAvisualnovo porque não houve alteração deHTML/CSS, nenhumLeadreal/joinWhatsApp.

Operação de31/out efetivamente concluída noledger e entregue pelaponteTelegram(recibo19335); hashdarespostafinalextraída verificado, não é evidência daentrega dehoje ou leitura humana. Sem enviodireto, ajuste deagendamento, serviços ou outrosperfis. Próximaleitura02/nov09hSãoPaulo:01/novcompleto, estado daautenticação/decisão#16, entrega/mix/iPhone e recibodesterelatório.
