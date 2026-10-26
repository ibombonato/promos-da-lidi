# ICB — Pesquisa de concorrentes e plano de experimentos estruturais

**Data:** 23/10/2026. **Status:** pesquisa concluída; hipóteses de backlog, não implementadas. **Escopo:** somente a landing experimental `index3.html`; nenhuma alteração de anúncios, rastreamento, destinos, controle, merge ou deploy.

## 1. Síntese executiva

**A oportunidade principal não é trocar mais cores: é tornar o valor do grupo concreto antes da entrada.** A página ICB promete curadoria de promoções, mas a renderização examinada não apresenta exemplo de mensagem/oferta, demonstração do processo, regras operacionais ou perguntas frequentes. Seu CTA já está inteiro na primeira dobra; não há evidência para tratar sua descoberta como um problema resolvido simplesmente movendo-o alguns pixels.[6]

A ModaPromos apresenta uma seção de mensagens de ofertas com imagens de perfumes, preço, cupom e loja.[2]

Só Perfumes Originais e AchadinhoVP colocam mensagens de redução de risco próximas do botão.[1][3]

Ninja organiza a oferta por assunto e explica funcionamento/regras.[4]

Curcio diferencia grupos gratuitos dos reservados a clientes, mas é uma loja, não um funil de afiliado equivalente.[5]

**Recomendação:** preservar CRO-001; concluir o fluxo de aprovação/publicação/avaliação do CRO-002; preparar em paralelo os módulos abaixo. Prioridade de oportunidade: demonstração real da oferta. Alternativa sem dependência de material: arquitetura da primeira dobra. Não lançar vários tratamentos simultaneamente nem substituir o experimento pendente sem decisão explícita.

## 2. Método e limites

- Busca pública em português por grupos de perfumes, achadinhos e ofertas; seleção intencional de cinco páginas, não um censo do mercado ou ranking de líderes.
- Conteúdo extraído e páginas renderizadas em Chromium real a **390×844**. Capturas da primeira dobra dos cinco concorrentes e da ICB, inspeção de seções inferiores/demonstrações e registros DOM. A página AchadinhoVP exigiu nova inspeção com rolagem nativa após timeout inicial.
- Domínios conhecidos de analytics/Meta bloqueados no navegador de auditoria. Nenhum CTA de entrada ativado, nenhum ingresso em grupos e nenhum anúncio alterado. Isso não garante ausência de qualquer registro server-side pelos sites visitados.
- **Não temos CVR, CPL, volume, público, testes internos ou faturamento desses concorrentes.** Uma prática observada gera hipótese; não prova que funciona, nem que funcionará para a ICB.
- Descontos, autenticidade, frequência, contagens de membros e alegações de privacidade são **afirmações dos respectivos sites**, não fatos auditados. Não copiar números, promessas ou urgência.
- Não foram feitas medições de Web Vitals de campo nem teste real de Safari. Imagens inicialmente não carregadas fora da tela podem ser lazy-loading: não classificá-las como quebradas sem rolagem e nova verificação.
- Pegar Promo/Pegar Perfumes apareceu em resultados sociais, mas não foi incluído na comparação de landing: não confirmei uma landing pública própria nesta rodada. Não substituí essa lacuna por um site presumido.

## 3. O que foi observado

### Só Perfumes Originais — concorrente de captação no mesmo nicho

**Observado:** primeira dobra compacta, foto com perfumes, foco explícito em perfumes originais, gratuidade, badge de membros e mensagem “Grupo oficial • Sem spam • Saia quando quiser” abaixo do CTA. O botão aparece em torno de y502 na captura390×844.[1]

**Aprendizado:** a proposta comunica categoria e confiança em um conjunto simples. Podemos testar confiança e transparência com evidências próprias, sem copiar design ou garantir autenticidade de lojas/produtos sem processo verificável.

**Cautela:** a extração textual e o navegador exibiram contagens de membros diferentes. Não uso nenhum desses números como evidência de tamanho ou sucesso do concorrente. A veracidade do badge não foi validada.

### ModaPromos / El Hombre — concorrente de grupos de perfumes

**Observado:** curadoria atribuída a pessoas identificadas, oferta de perfumes nacionais/importados, mensagens de gratuidade/saída junto ao botão, cartões explicando benefícios, CTAs repetidos e seção “Veja algumas promoções do grupo”. Na inspeção visual após rolagem, há mensagens com imagem de perfume, preço anterior/atual, cupom e referência de loja.[2]

**Aprendizado:** mostrar o produto do grupo — a mensagem que o visitante receberá — é uma hipótese mais forte de compreensão do valor do que apenas listar benefícios abstratos. A página também fornece argumentos para quem precisa de mais informação antes de entrar.

**Cautela:** descontos e “vagas limitadas” são alegações não auditadas; não serão transplantados para a ICB. As capturas iniciais de uma seção inferior exibiam espaços vazios; a nova rolagem mostrou a oferta. O relatório usa a inspeção posterior, não conclui falha generalizada. Nenhum preço/cupom do concorrente está sendo recomendado como oferta vigente.

### AchadinhoVP — concorrente de achadinhos generalistas

**Observado:** CTA na primeira dobra, pontos de gratuidade/liberdade logo abaixo, explicação “Só admin publica” e seção “É assim que as ofertas chegam”; o rodapé declara possibilidade de comissão e variação de preços.[3]

**Aprendizado:** o visitante não decide só se gosta de descontos: precisa saber se terá conversa excessiva, como recebe a oferta e se há compromisso. Esse é um módulo de redução de objeções e transparência, não apenas uma nova frase no botão.

**Cautela:** existe elemento de vídeo com `/assets/preview.mp4`, mas, na sessão auditada, permaneceu com `readyState=0`, tempo0 e área preta. **Não assisti ao conteúdo e não afirmo que o vídeo funciona para todos ou que converte melhor.** Para a ICB, qualquer demonstração precisa ter poster/fallback e não depender de autoplay. Promessas de até80%OFF, vagas ou entrada em5segundos não foram validadas.

### Ninja das Ofertas — referência de relevância temática e funcionamento

**Observado:** escolha de assuntos, incluindo perfumes/beleza, cartões de entrada e seções de funcionamento e perguntas frequentes. A primeira dobra também contém um painel de contagens/alegações de atividade antes do primeiro cartão geral.[4]

**Aprendizado:** explicar relevância e regras pode reduzir incerteza. Contudo, copiar dezenas de categorias para uma landing de tráfego já interessado em perfumes adicionaria escolhas e desviaria do objetivo.

**Cautela:** não verifiquei contagens/descontos ou privacidade de cada destino. Não prometer “ninguém vê seu número” para um grupo normal da ICB com base na promessa de outro serviço/canal. Não criar novos grupos, seletores ou destinos sem autorização.

### Curcio Parfum — referência adjacente, não comparação equivalente

**Observado:** separação explícita entre grupos abertos gratuitos e grupos fechados exclusivos para clientes, descrição de benefícios e identidade de loja. Na captura mobile há navegação comercial e bastante texto antes do convite.[5]

**Aprendizado:** explicar o que cada pessoa pode esperar e quem pode participar torna o contrato da oferta claro. Não devemos copiar a distinção de grupos fechados se essa operação não existir na ICB.

**Cautela:** loja com base de clientes tem contexto de confiança e intenção diferente de visitante frio vindo do Meta. Não inferir superioridade ou necessidade de alongar nossa página pelo exemplo.

### ICB — diagnóstico comparativo

**Observado:** headline de perfumes, curadoria em primeira pessoa, foto da Lidi, CTA único, número/estrelas de prova social e grade de seis benefícios; sem exemplo concreto de mensagem, FAQ ou explicação operacional no HTML público examinado. O CTA está em y503,75–565,75 e a página tem1068px de altura em390×844, sem overflow horizontal.[6]

**Conclusão de UX:** a ICB já é clara sobre produto/canal e permite entrar sem formulário na própria landing. A lacuna prioritária é **evidência do valor e previsibilidade da experiência**, não ausência de CTA na primeira dobra. A autoria existe visualmente, mas seu processo de curadoria não é demonstrado. A afirmação16.000/estrelas continua sem comprovação fornecida nesta análise.

## 4. Roadmap priorizado — propostas, não novos experimentos publicados

IDs `BL-*` são itens de backlog; só atribuir o próximo ID `CRO-*` quando houver implementação real. ICE é julgamento qualitativo de impacto/confiança/facilidade, não previsão de lift ou score estatístico.

| Ordem de oportunidade | Backlog | Mudança principal | ICE | Gate |
|---|---|---|---|---|
| 1 | BL-01 — Demonstrar o conteúdo real | Módulo de exemplos reais de ofertas/mensagens | I9/C6/E6 | Três ofertas próprias verificáveis e autorização |
| 2 | BL-02 — Arquitetura orientada à oferta | Reestruturar somente a primeira dobra, reduzindo domínio do branding | I8/C5/E8 | Sem material extra; elegível após CRO-002 |
| 3 | BL-03 — Contrato de funcionamento | Módulo de regras e objeções antes do compromisso | I8/C6/E8 | Confirmar regras reais do grupo |
| 4 | BL-04 — Curadoria demonstrada | Prova de processo/autoria em módulo único | I7/C5/E5 | Método verificável e material real da Lidi |
| Condicional | BL-05 — Recuperar ação após leitura | CTA contextual quando o principal sair da tela em uma página mais longa | I5/C4/E7 | Só se módulos anteriores criarem essa necessidade |

### BL-01 — “Veja o que chega no seu WhatsApp”

**Problema:** o visitante precisa imaginar o conteúdo do grupo a partir de benefícios genéricos. **Evidência:** ausência na ICB e demonstração de mensagens na ModaPromos.[2][6]

**Hipótese:** visualizar uma oferta realmente enviada, com formato e contexto, aumenta a compreensão do benefício e a propensão à entrada.

**Tratamento:** acrescentar um único módulo de demonstração abaixo do CTA principal, antes da seção genérica de benefícios. Usar um exemplo principal legível e até dois exemplos complementares, sem carrossel obrigatório. Mostrar produto, imagem autorizada, loja, preço/cupom quando verificáveis e data do envio. Não trocar headline, CTA, foto, prova social ou outras seções nesse mesmo teste.

**Regras:** conteúdo próprio, autorizado e anonimizado; nada de copiar mensagens concorrentes, fabricar conversa ou inserir produto/preço ilustrativo como real. Se histórico, rotular “Exemplo enviado emDD/MM; preço e estoque podem mudar”, sem sugerir oferta atual. A imagem é uma demonstração, **não um link concorrente para comprar fora do funil**; manter destino WhatsApp existente e não adicionar CTAs para lojas. Ofertas atuais exigem processo de atualização/retirada antes de prometer atualidade.

**Impacto esperado:** reduzir “o que vou receber?”; não previsão de aumento percentual. **Avaliação:** Lead/LPV principal, CPL secundário; atenção a carregamento da imagem e eventual deslocamento dos argumentos. **Risco:** exemplo irrelevante, ilegível, expirado ou que distraia da entrada.

**Dependência concreta:** três ofertas reais da própria operação, com origem/data/produto/loja/preço/cupom e autorização de exibição; um print sem nomes, telefones, fotos ou IDs pessoais. A imagem final precisa continuar legível em360px.

### BL-02 — Primeira dobra de oferta, não de cartaz

**Problema:** a área visual de marca/foto ocupa uma parte importante do início, antes do benefício. O CTA já aparece sem rolagem; a hipótese não é “colocá-lo na dobra”, mas mudar a hierarquia para que o visitante compreenda a oferta e veja mais argumento útil no primeiro viewport.[6]

**Tratamento:** reestruturar o módulo inicial: marca compacta, foto menor ainda reconhecível, headline do CRO-001 preservada, mesma copy e mesmo CTA. Reduzir a altura do cabeçalho decorativo e aproximar benefício/ação; não adicionar descontos, urgência, números, demonstração de ofertas ou FAQ no mesmo teste. Meta visual de projeto: CTA aproximadamente na região320–380px, a confirmar em protótipo — **não uma medida já validada**.

**Por que é estrutural:** muda a arquitetura de informação do módulo, não uma propriedade isolada. O resultado avaliaria o conjunto dessa hierarquia; não permitiria atribuir ganho individual à foto ou a um espaçamento.

**Avaliação:** Lead/LPV e CPL; checagens de legibilidade, foto/autoria, primeira dobra e estabilidade de layout. **Risco:** perder vínculo pessoal/identidade em busca de compactação. Não remover a Lidi nem alterar promessa como variável adicional.

**Dependência:** nenhuma oferta/depoimento adicional. **Alternativa prática:** se BL-01 estiver bloqueado por material quando CRO-002 for avaliado, executar BL-02 em vez de esperar sem prazo.

### BL-03 — Como funciona, sem surpresas

**Problema:** entrar em grupo pode implicar receio de conversa, excesso de mensagens, custo ou falta de controle. Os concorrentes tratam essas objeções; isso é pista para hipótese, não evidência de que sejam as objeções principais do nosso público.[1][3][4]

**Tratamento:** um módulo curto e escaneável com o fluxo real: tocar no botão → abrir o convite no WhatsApp → confirmar a participação/solicitar aprovação, conforme a configuração real. Acrescentar respostas sobre custo, quem publica, tipo/ritmo de conteúdo e saída. Não mudar convites ou exigir cadastro, telefone, quiz ou permissões extras.

**Conteúdo condicionado a confirmação:** “Só administradores publicam” e frequência/horários só entram se forem verdadeiros. Não garantir anonimato de número, ausência absoluta de mensagens indesejadas ou entrada instantânea. “Sem cadastro na landing” descreve a página, não elimina os passos do WhatsApp.

**Avaliação:** Lead/LPV/CPL. Não usar aberturas de FAQ como nova definição de conversão. **Risco:** explicação longa criar mais esforço; limitar a dúvidas essenciais e preservar a ação principal.

**Dependência concreta:** confirmação de quem pode publicar, necessidade de aprovação e faixa realista de frequência. Não prometer reduzir a frequência ou alterar a operação do grupo para adaptar a copy.

### BL-04 — Mostrar a curadoria em vez de apenas afirmá-la

**Problema:** a foto e “eu garimpo” identificam uma pessoa, mas não explicam por que confiar na seleção. A autoria/curadoria é enfatizada em outros funis e pode ser demonstrada com material próprio.[2][3][6]

**Tratamento inicial:** um módulo de processo real, com a Lidi e um exemplo verificável do que confere antes de indicar. Escolher **um formato por teste**: primeiro uma demonstração estática curta; vídeo é uma hipótese posterior/alternativa, não pacote simultâneo com novo layout, FAQ e prova social.

**Roteiro proposto, não afirmação pronta:** “Aqui está uma oferta que enviei; aqui está o que conferi; é nesse formato que você recebe no grupo”. Critérios de preço, cupom, loja/vendedor e produto precisam corresponder à prática real. Não declarar “sempre o menor preço”, originalidade garantida ou validação infalível sem suporte.

**Se for vídeo:** gravação real curta, legendada, poster legível e reprodução opcional; carregar mídia sob demanda. Sem autoplay obrigatório, dependência pesada ou acesso ao grupo condicionado a assistir. A seção do AchadinhoVP mostrou por que a intenção de demonstrar não basta quando a mídia não fica visível na sessão.[3]

**Avaliação:** Lead/LPV, CPL e integridade de carregamento. Não adicionar eventos de Pixel nem medir sucesso por reproduções. **Risco:** custo/performance, promessa não sustentada e conteúdo que vira distração.

**Dependência:** método confirmado e autorização de imagem/conteúdo; material existente pode substituir nova gravação. A alegação16.000/estrelas não será ampliada; sua comprovação permanece pendente, e qualquer substituição da prova social será registrada como intervenção própria, não embutida aqui.

### BL-05 — CTA acessível após consumir a demonstração (condicional)

**Problema futuro:** se a página ganhar conteúdo substancial, a pessoa pode terminar a leitura longe do CTA. ModaPromos e AchadinhoVP repetem chamadas de entrada após argumentos.[2][3]

**Por que não agora:** a ICB atual é curta; em390×844 a rolagem máxima observada não leva o CTA para fora do viewport. Não há fundamento para instalar uma barra fixa agora só porque é uma prática comum.[6]

**Tratamento elegível:** após uma versão mais longa ser mantida, testar um CTA final ou barra contextual que só apareça quando o principal sair da tela — escolher um, não ambos. Mesma promessa e mesmo destino; não cobrir conteúdo, teclado ou controles de acessibilidade. Preservar semântica/contagem do Lead, sem criar novo evento ou disparo duplicado; se a implementação exigir mudar a definição de tracking, solicitar autorização antes.

**Avaliação:** Lead/LPV, CPL e regressões mobile. **Risco:** intrusão e duplicação de eventos. Essa hipótese é complementar, não o centro do novo programa.

## 5. Ordem de execução e regras de decisão

1. **Agora:** CRO-002 continua no PR#16, sem publicação por esta pesquisa; preservar o tratamento. Preparar material, arquitetura e especificações dos itens acima sem mudar a exposição dos visitantes.
2. **Depois da avaliação do CRO-002:** BL-01 se houver material; caso contrário BL-02. A prioridade por potencial não vira bloqueio de execução por dependência opcional.
3. Avaliar explicitamente o primeiro teste estrutural e manter/reverter por aprovação humana quando apropriado; só depois BL-03 ou o próximo item com evidência melhor. Não acumular cinco mudanças e chamar cada uma de vencedora.
4. Um módulo inteiro pode ser uma intervenção principal. Registrar que o resultado pertence ao módulo/conceito, não às subpartes; isso permite testar alterações maiores sem fingir isolamento impossível.
5. Para **os futuros testes deste roadmap**, formar referência apenas com dias completos da versão imediatamente anterior, preferencialmente os últimos7dias comparáveis, ampliando se faltar volume/cobertura. Não usar14dias que misturem tratamento anterior só para preencher uma janela. Confirmar publicação/SHA, excluir dia misto e pré-registrar regras antes de observar o pós. Essa proposta de desenho futuro não altera silenciosamente o plano já registrado do CRO-002.
6. Métrica principal invariável: **Lead atribuído/LPV**, proxy de clique, não participante confirmado. CPL secundário; controle apenas contexto observacional. Registrar mudanças de anúncios, orçamento, dispositivo/posicionamento e revisões de atribuição.
7. Calcular IC95%, mudança absoluta/relativa e evolução do controle. Checkpoint com volume suficiente e cobertura de dias da semana, sem vitória por primeiro p-valor diário ou apenas por número de dias. Se continuar sem suporte, encerrar Inconclusivo; não aguardar significância indefinidamente.

### Planejamento de volume — referência, não promessa de lift

Usando **somente para ilustração de planejamento** o snapshot de23/out já coletado (experimental16–22/out:1676/4380=38,26%,625,71LPV/dia), duas proporções independentes, alfa bilateral5%,poder80%:

| MDE de planejamento | LPV aproximadas por período | Dias para volume no ritmo histórico |
|---|---:|---:|
| +3p.p. | 4177 | 7 |
| +5p.p. | 1516 | 3 |

**Esses números não são previsão de ganho nem prazo de vitória.** Atualizar baseline/MDE/cálculo quando cada teste ficar elegível; dependência entre eventos, atribuição e desenho não randomizado limitam o modelo. Atingir1516LPV em poucos dias não elimina a necessidade de cobertura semanal e avaliação de mix. A pesquisa não fez nova consulta de métricas Meta; não tratar o snapshot como dados posteriores.

## 6. Materiais e limites práticos

A solicitação anterior de três ofertas próprias e um print anonimizado continua válida; não é uma nova cobrança diária. Este plano explica o que ela desbloqueia: **BL-01 e preparação de BL-04**. Também confirmar regras reais para BL-03 e comprovação/autorização do número16.000 já existente. Nenhum material de concorrente será usado como prova social ou oferta da ICB.

**Não priorizado:** copiar percentuais de desconto/contadores; falsa escassez; quiz obrigatório; novas categorias/grupos ou destinos; formulário para telefone; remover o vínculo pessoal da Lidi; redesenhar tudo junto; vídeo automático pesado; trocar a definição de conversão. Segmentar grupos ou medir entradas confirmadas exigiria escopo/autorização e instrumentação próprios.

**Critério de avanço diário durante a espera:** preparar wireframe do módulo escolhido, selecionar/validar materiais autorizados, formular copy fiel à operação, pré-registrar comparação e checar publicação/avaliação. Repetir apenas o título do backlog não conta como avanço.

## 7. Evidências locais

Artefatos em `/home/ibombonatohermes/work/hermes-scratch/cro-competitors-2026-10-23/`: `comparativo-mobile.png`, capturas individuais em `screenshots/`, DOM/textos das seis páginas, `browser-audit.json`, `achadinho-media.json`, `extracted.json`, `planning.json` e `sources.json` com citações e evidências literais. Screenshots documentam a sessão, não performance comercial. O comparativo inclui cinco concorrentes + ICB; os números comerciais visíveis são alegações não validadas.

## Sources

[1] https://soperfumesoriginais.com
[2] https://modapromos.com.br/perfumes
[3] https://achadinhovp.com.br
[4] https://grupo.ninjadasofertas.com
[5] https://curcioparfum.com/pages/grupos
[6] https://www.lidimelo.com.br/index3.html
