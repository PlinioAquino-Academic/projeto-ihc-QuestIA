# Feedback de Correção — Projeto de IHC: QuestIA

**Projeto avaliado:** `projeto-ihc-main.zip`  
**Tema identificado:** QuestIA — interface para interação com algoritmo de correção automática de questões dissertativas do ENADE.  
**Equipe identificada no README:** Arthur Soares Sousa e Danilo David Miranda.  


## Síntese avaliativa

O projeto apresenta uma linha conceitual coerente: parte de um problema real — dificuldade de correção rápida, justa e transparente de respostas dissertativas — e mantém esse problema como eixo em personas, cenários, tarefas, protótipos, modelo conceitual, MoLIC e avaliação. Esse é um ponto forte importante, pois em IHC espera-se rastreabilidade entre **usuário, contexto de uso, tarefa, requisitos, interação e avaliação**.

A equipe demonstra boa compreensão do domínio educacional e faz uma escolha pertinente ao trabalhar com dois perfis primários: professor corretor e aluno em preparação para o ENADE. Também há bons indícios de prototipação, telas de alta fidelidade, uso de dashboards, feedback instantâneo e preocupação com explicabilidade da correção automatizada.

Entretanto, a entrega possui falhas relevantes de completude formal e metodológica. Os pontos mais frágeis estão em **coleta de dados**, **avaliação por observação do usuário**, **avaliação heurística**, **análise de concorrência** e em alguns itens de formalização exigidos no enunciado. Em alguns casos, há boa intenção conceitual, mas faltam instrumentos, protocolos, tabelas, autoria por integrante, evidências completas ou alinhamento exato com o método solicitado.

Um ponto de atenção para toda a correção: o ZIP do projeto contém os arquivos Markdown, mas não contém as imagens incorporadas localmente. As imagens aparecem como links externos do GitHub (`user-attachments`). Assim, foi possível verificar a existência de referências a telas e diagramas, mas não validar com plena segurança todos os detalhes internos de cada imagem, como operadores CTT, sintaxe completa dos diagramas MoLIC, presença de caixa preta, fluxos tracejados, inputs e outputs. Essa limitação está indicada nos itens afetados.

## Quadro geral de conformidade por assunto

| Assunto avaliado | Situação | Comentário sintético |
|---|---:|---|
| Conhecimento do problema | **Parcialmente atendido** | A descrição, objetivo, usuários, benefícios, tecnologias, funcionalidades e contexto estão presentes; faltam itens formais do modelo, como matrícula, título/orientação em campos específicos e estrutura completa de perguntas. |
| Análise de concorrência | **Parcialmente atendida** | Há concorrentes representativos e imagens para parte deles; faltam público-alvo explícito, análise de UX/opiniões, referências e principalmente padrões/tendências de mercado descritos de forma sistemática. |
| Personas, empatia, contexto e jornada | **Parcialmente atendidos** | Personas estão bem alinhadas ao projeto; faltam fotos de rosto, ganhos no mapa de empatia, maior caracterização social/econômica/cultural e dados que o produto deve guardar. |
| Cenários de análise/problema | **Parcialmente atendidos** | Há dois cenários e questões de refinamento por elemento; um cenário descreve a solução QuestIA, quando deveria narrar somente o problema atual. |
| Análise de tarefas — HTA, GOMS e CTT | **Parcialmente atendida** | Há 2 HTAs, 2 GOMS e 2 CTTs, coerentes com os 2 integrantes; a estrutura é promissora, mas faltam evidências verificáveis das imagens e maior rigor em algumas regras de seleção e concorrência. |
| Prototipação | **Atendida com ressalvas** | Há telas, teste com usuários e refinamento visual; faltam numeração formal das telas, fluxos explícitos, identificação de botões/estados e relatório mais sistemático. |
| Coleta de dados | **Insuficiente** | Foram entregues questionários, mas faltam as três técnicas diferentes, protocolo de aplicação, aspectos éticos e a separação clara entre “que dados coletar” e “de quem coletar”. |
| Ciclo de vida da engenharia de usabilidade | **Atendido com ressalvas** | Plataforma, princípios e metas estão presentes; metas quantitativas precisam virar critérios mensuráveis, não apenas pesos percentuais. |
| Modelo conceitual | **Parcialmente atendido** | Há cenários de interação, DCC, mapas de objetivo e tabela unificada de signos; alguns diálogos usam detalhes de interface e há falas atribuídas ao usuário que deveriam ser do sistema. |
| MoLIC | **Parcialmente atendida** | Há dois diagramas referenciados, metáforas e tratamento de rupturas; não foi possível validar completamente a sintaxe visual porque as imagens não estão no ZIP. |
| Figma / telas finais | **Atendido** | Há link para protótipo e telas finais descritas; atende ao espírito da exigência. |
| Planejamento da avaliação — DECIDE | **Atendido com ressalvas** | A tabela DECIDE está completa e coerente; poderia detalhar melhor os instrumentos e critérios de análise. |
| Inspeção heurística | **Parcialmente atendida / insuficiente para a exigência completa** | Há severidade, prints referenciados e sugestões, mas só foram apontados 2 problemas e 1 boa prática; faltam avaliações por integrante e cobertura de todas as telas. |
| Observação do usuário | **Insuficiente** | Há relatos de dois professores, mas faltam fluxograma, procedimento de preparação, tabela de resultados por tarefa, tempo, erros, satisfação, vídeos e respostas de formulário. |

## Conhecimento do problema

A equipe apresenta uma descrição clara do QuestIA: uma interface para interação com um algoritmo de correção automática de questões dissertativas do ENADE. O objetivo também está bem formulado, pois combina dois benefícios de IHC relevantes: **redução de tempo** e **redução de discrepância na avaliação**. A definição de usuários finais contempla dois grupos coerentes, professores corretores e alunos em preparação para o exame.

O item mais importante dessa parte, segundo as regras, é a explicitação de funcionalidades na visão do usuário. Nesse ponto, o projeto atende bem: há mais funcionalidades do que o número de integrantes do grupo. Para o professor, aparecem dashboard estratégico, mapa de calor, métricas de discrepância e relatório de lacunas de aprendizado. Para o aluno, aparecem feedback instantâneo, comparativo com a referência e histórico de evolução. Essas funcionalidades são relevantes e se mantêm presentes em outras partes do trabalho, o que melhora a consistência geral do projeto.

Conceitualmente, a equipe compreende que o contexto de uso é diferente para professor e aluno. Esse cuidado é importante porque a usabilidade não é uma propriedade abstrata da tela; ela depende de usuário, objetivo, tarefa, equipamento e ambiente. Um professor em longa sessão de correção possui necessidades diferentes de um estudante realizando simulado em ambiente doméstico ou escolar.

Pontos que precisam ser corrigidos ou complementados:

- O modelo original solicitava campos específicos, como membros com nome completo e matrícula, título original do TCC, nome do orientador, indicação explícita sobre interface, objetivo, produto final, usuário final, benefícios, funcionalidades, tecnologias e contexto de uso. Parte dessas informações aparece no README, mas não no formato completo solicitado.
- A matrícula dos integrantes não foi informada.
- O produto final poderia ser descrito de forma mais precisa: por exemplo, “plataforma web de apoio à correção e treinamento de questões dissertativas do ENADE”, em vez de apenas “interface”.
- O contexto de uso poderia indicar melhor condições de uso: tempo disponível, pressão institucional, equipamentos, conectividade, privacidade dos dados, ambiente físico e limitações cognitivas decorrentes de fadiga.

**Recomendação de melhoria:** reescrever essa seção no formato do modelo, respondendo explicitamente cada pergunta. A qualidade conceitual está boa, mas a completude formal ainda não está equivalente ao conteúdo da aula.

## Análise de concorrência

A equipe identificou três grupos de soluções comparáveis: ferramentas de IA generativa, plataformas de dashboard/BI e ambientes virtuais de aprendizagem. A escolha é adequada, pois o enunciado deixa claro que concorrente não precisa ser uma solução idêntica; pode ser uma solução que atua na mesma área ou que o público-alvo usa para realizar tarefas semelhantes. Nesse sentido, ChatGPT/Gemini, Grafana/Qlik e Moodle/Google Classroom são bons referenciais.

Também há um ponto positivo na forma como a equipe diferencia o QuestIA: a especialização em ENADE, a integração com critérios de banca, a existência de métricas de discrepância e dashboards pedagógicos. Essa comparação ajuda a justificar o valor do sistema do ponto de vista do usuário.

O trabalho inclui imagens para os dois primeiros grupos de concorrentes. Isso é importante porque a principal função pedagógica da análise de concorrência em IHC é observar **padrões de interação**, **organização visual**, **affordances**, **linguagem**, **feedback**, **navegação** e **tendências de interface**. Os prints servem como insumo para decisões futuras de prototipação e avaliação heurística.

Pontos que precisam ser corrigidos ou complementados:

- Não há uma seção inicial clara de **público-alvo** dentro da análise de concorrência.
- O item de **experiência do usuário, satisfação, avaliações ou opiniões** não foi desenvolvido. A equipe poderia ter analisado comentários de usuários, limitações percebidas, reclamações comuns e vantagens de cada solução.
- O item de **padrões e tendências de mercado**, considerado o mais importante pelas regras, não aparece de forma explícita. A equipe descreve pontos fortes e fracos, mas não sistematiza tendências como: uso de cartões de métricas, dashboards com gráficos de tendência, feedback visual por cor, comparações lado a lado, uso de filtros, histórico, alertas e linguagem explicativa.
- O terceiro grupo, Moodle/Google Classroom, não possui prints incorporados, diferentemente dos dois primeiros grupos.
- Faltam referências organizadas. Mesmo que os preços sejam ignorados conforme a regra, os links de origem e as imagens deveriam ser acompanhados de fonte.

**Como completar:** criar uma tabela de padrões observados, por exemplo: “cards de indicadores”, “mapa de calor”, “comparação lado a lado”, “histórico filtrável”, “feedback por cores”, “alertas contextuais”, “hierarquia visual”, “linguagem natural no feedback”. Para cada padrão, indicar em qual concorrente aparece e como o QuestIA pretende adaptar esse padrão ao contexto educacional.

## Personas, mapa de empatia, contexto de uso e jornada do usuário

As personas Roberto Almeida e Beatriz Costa são coerentes com o problema. A primeira representa o professor corretor, preocupado com justiça, fadiga, produtividade e consistência. A segunda representa a estudante em preparação, preocupada com feedback imediato, clareza dos critérios e ansiedade diante de respostas dissertativas. Essa separação entre perfis é um acerto importante, pois o projeto não tenta tratar todos os usuários como se tivessem a mesma motivação.

As jornadas narrativas também são um ponto positivo. Elas mostram começo, desenvolvimento e resultado da interação com o QuestIA. A jornada do professor evidencia a carga cognitiva da correção em massa e a necessidade de apoio à decisão. A jornada da aluna mostra a insegurança diante de gabaritos estáticos e a transformação do feedback em aprendizado. Esses elementos estão bem conectados às funcionalidades propostas.

Do ponto de vista teórico, personas devem condensar conhecimento sobre usuários reais ou presumidos de forma útil ao projeto. Elas não devem ser apenas perfis demográficos; precisam orientar decisões de interface. O projeto consegue fazer isso em parte, pois as dores das personas aparecem depois em tarefas, cenários e protótipos.

Pontos que precisam ser corrigidos ou complementados:

- As personas não possuem foto de rosto, requisito explícito do enunciado.
- A caracterização demográfica, comportamental e psicográfica aparece, mas ainda falta maior detalhamento de contexto social, econômico e cultural. Por exemplo: tipo de instituição, nível de familiaridade com plataformas educacionais, acesso a dispositivos, disponibilidade de tempo e possíveis limitações de conectividade.
- O mapa de empatia possui “vê”, “ouve”, “pensa e sente”, “fala e faz”, mas não apresenta explicitamente os campos **dores** e **ganhos**. As dores aparecem nas personas, mas o mapa deveria incorporar também ganhos/benefícios esperados.
- O enunciado solicitava indicar quais informações sobre o usuário o produto deve guardar. Isso não aparece de forma explícita. O QuestIA provavelmente precisaria armazenar perfil, papel do usuário, histórico de simulados, respostas submetidas, notas, critérios utilizados, revisões do professor e preferências de acessibilidade.
- O contexto de uso descreve ambientes físicos, mas poderia desenvolver melhor o contexto social, econômico e cultural. Também faltou responder o que normalmente deve estar acontecendo no ambiente quando o usuário interage com o produto.

**Recomendação de melhoria:** manter as duas personas primárias, mas inserir foto, dados comportamentais mais completos, informações que o sistema deve armazenar e um mapa de empatia com dores e ganhos. A ausência de persona secundária não deve ser tratada como falha grave, conforme a própria regra de correção.

## Cenários de análise/problema

A equipe entregou dois cenários, o que é adequado para um grupo com dois integrantes. O segundo cenário, sobre a incerteza do estudante Lucas ao comparar sua resposta com o padrão oficial do INEP, atende bem à proposta de “história triste”: ele descreve a situação problemática antes da solução, evidencia frustração, incerteza, falta de feedback e ansiedade.

As questões de refinamento foram estruturadas pelos elementos do método: ambiente/contexto, atores, objetivos, planejamento, ações, eventos e avaliação. Isso é um ponto positivo, porque demonstra que a equipe conhece a estrutura conceitual do cenário e não está apenas escrevendo uma narrativa livre.

O refinamento com marcações entre colchetes também aparece. Essa prática é importante porque evidencia como as perguntas de refinamento realmente melhoraram o cenário inicial, acrescentando detalhes relevantes.

Pontos que precisam ser corrigidos ou complementados:

- O primeiro cenário já inclui o uso do QuestIA como solução. O enunciado afirma que o cenário de análise/problema não deve descrever a solução; deve descrever o problema existente na atualidade. Portanto, esse cenário deveria narrar a correção manual ou semi-manual de respostas dissertativas, sem ainda introduzir a interface QuestIA como apoio.
- No primeiro cenário, o “Sistema QuestIA” aparece como ator. Para cenário de problema, isso enfraquece a atividade, pois o objetivo era caracterizar a situação antes da intervenção de design.
- As perguntas de refinamento poderiam ser formuladas como perguntas ainda não respondidas pelo cenário inicial. Algumas perguntas estão adequadas, mas outras ficam genéricas e poderiam explorar mais restrições reais: volume de provas, critérios de correção, cansaço, recursos disponíveis, forma atual de registro de notas e risco de inconsistência.
- A narrativa refinada deveria destacar com mais clareza quais trechos foram acrescentados em relação à versão original. O uso de `[Q1]`, `[Q2]` etc. ajuda, mas seria melhor usar colchetes em torno do próprio texto novo.

**Exemplo de correção conceitual:** em vez de “ele utiliza o sistema QuestIA”, o cenário do professor deveria começar com “Ricardo recebe 120 respostas dissertativas em arquivos separados, abre uma planilha para registrar notas e consulta manualmente o padrão de resposta do INEP”. A partir disso, a dor de inconsistência, fadiga e falta de visão global ficaria mais clara.

## Análise de tarefas — HTA, GOMS e CTT

A equipe apresentou duas tarefas principais: envio de resposta e obtenção de feedback pelo aluno; análise da correção e desempenho da turma pelo professor. Essa escolha é coerente com as funcionalidades centrais do QuestIA e com as duas personas primárias. Para um grupo de dois integrantes, a quantidade mínima de diagramas também está adequada: há duas estruturas HTA, duas modelagens GOMS e duas referências de CTT.

Na HTA, a atividade zero foi representada com input, feedback e plano, o que atende a uma regra importante. As demais atividades não repetem input/feedback de forma indevida, e aparecem recomendações e problemas em pelo menos algumas linhas. Isso mostra entendimento de que HTA não é apenas fluxograma; é uma decomposição hierárquica de metas e subtarefas.

Na GOMS, há decomposição em goals, methods, selection rules e operators. O uso de operadores como clicar, selecionar, digitar, analisar e verificar está adequado ao tipo de tarefa modelada. A equipe também diferencia métodos alternativos, por exemplo selecionar questão antes de escrever ou escrever diretamente quando a questão já está selecionada.

Pontos que precisam ser corrigidos ou complementados:

- A regra menciona “pelo menos 4 funcionalidades diferentes”. A equipe trabalhou com duas macrofuncionalidades. Como o grupo tem dois integrantes, a quantidade de diagramas está coerente; porém, para ficar mais completo, poderia desdobrar em quatro funcionalidades: selecionar simulado, submeter resposta, interpretar feedback, consultar dashboard/relatório.
- A HTA deveria deixar mais explícita a estrutura de árvore binária sem fluxos. Como as imagens não estão locais no ZIP, não foi possível validar plenamente se os diagramas visuais seguem essa exigência.
- Na GOMS, sempre que houver método alternativo, a regra de seleção deve aparecer imediatamente associada ao método. A maioria dos casos atende, mas o método “Monitorar níveis de fadiga” não apresenta uma regra de seleção tão explícita quanto os demais.
- Alguns operadores são cognitivos, como “raciocinar” e “avaliar”. Isso pode aparecer em GOMS, mas é recomendável diferenciar operadores perceptivos, motores e cognitivos com mais rigor quando o objetivo for estimar esforço ou tempo.
- Nos CTTs, há imagens referenciadas e legenda, mas não foi possível validar visualmente a existência de concorrência entre tarefas, operadores temporais ou decomposição adequada, porque os arquivos das imagens não estão no ZIP.

**Recomendação de melhoria:** transformar cada diagrama em uma entrega verificável também por texto. Por exemplo, para o CTT, listar abaixo da imagem quais relações temporais foram usadas: sequência, escolha, concorrência, interrupção, iteração. Isso tornaria a análise independente da visualização da imagem.

## Prototipação

A prototipação é uma das partes mais fortes do trabalho. A equipe apresenta telas para input de resposta, feedback do modelo, dashboard do professor, consistência/desempenho e histórico de provas corrigidas. Também há registro de teste com dois professores da FEI e indicação de alterações posteriores em cor e tamanho de fonte.

Do ponto de vista de IHC, é positivo que a equipe tenha usado o protótipo como instrumento de aprendizagem e não apenas como ilustração. O ciclo “produzir tela → apresentar a usuários → coletar críticas → alterar tela” está alinhado à lógica de design centrado no usuário e avaliação iterativa.

Pontos que precisam ser corrigidos ou complementados:

- O enunciado pedia identificação das tarefas e objetivos mais importantes para o usuário. As telas sugerem essas tarefas, mas elas não foram listadas formalmente antes do protótipo.
- A equipe não descreveu fluxos de interação entre telas. Há várias telas, mas faltam setas, estados ou uma explicação textual do caminho: início, escolha da questão, resposta, submissão, processamento, feedback, histórico.
- As telas não estão numeradas segundo um fluxo completo. Há “Tela 1” e “Tela 2”, mas dentro delas existem múltiplas variações e estados.
- Botões e elementos de mudança de estado não foram explicitamente indicados, como “Enviar”, “Cancelar”, “Ver feedback”, “Filtrar”, “Gerar relatório”.
- O relatório de teste com usuários é muito resumido. Seria melhor incluir uma tabela com usuário, tarefa executada, observações, crítica, decisão de redesign e evidência da tela alterada.
- O requisito mencionava protótipo em papel, mas as regras aceitam também telas prontas do sistema. Portanto, o uso de telas digitais não deve ser penalizado, desde que o processo de prototipação e teste esteja documentado.

**Recomendação de melhoria:** criar uma subseção “Fluxo de interação prototipado” com as telas numeradas e as transições entre elas. Isso aproximaria a entrega solicitada que costumam evidenciar melhor a sequência de interação.

## Coleta de dados

Esta é uma das partes mais frágeis da entrega. A equipe escolheu questionários e justificou o método, afirmando que permite coletar dados de muitos usuários de forma rápida e barata. Essa justificativa é adequada. Também há uma boa enumeração de tipos de dados: perfil do usuário, relação com tecnologia, conhecimento do domínio e tarefas, motivações e valores.

Entretanto, a exigência da atividade não era apenas indicar questionários. Para um grupo com dois integrantes, as regras solicitam ferramentas de coleta com técnicas diferentes, sendo questionário uma delas. A lista de técnicas ensinadas inclui entrevistas, questionários, grupos de foco, brainstorming, classificação de cartões, estudos de campo e investigação contextual.

Pontos que precisam ser corrigidos ou complementados:

- Faltam as perguntas explícitas de identificação de necessidades: **que dados coletar?** e **de quem coletar?**. A equipe lista tipos de dados, mas não separa claramente as fontes: alunos concluintes, professores corretores, coordenadores de curso, docentes que aplicam simulados etc.
- Faltou a seção de **aspectos éticos**. Para este projeto, ela é essencial, porque envolve dados educacionais, desempenho acadêmico, respostas dissertativas, uso de IA e possível assimetria de poder entre professor e aluno.
- Foram entregues apenas questionários. Faltam outras técnicas, como entrevista com professores corretores, investigação contextual da rotina de correção ou grupo focal com alunos.
- Faltou explicar como aplicar cada instrumento: tempo estimado, forma de convite, critérios de inclusão, ambiente de aplicação, ordem das perguntas, forma de registro e garantia de anonimato.
- Os links de formulário foram apresentados, mas o conteúdo das perguntas não foi transcrito no repositório. Isso dificulta a avaliação do instrumento, pois o avaliador depende de acesso externo.

**Como completar:** incluir pelo menos três instrumentos: questionário com alunos, entrevista semiestruturada com professores e investigação contextual ou estudo de campo durante uma rotina de correção. Para cada instrumento, apresentar nome, objetivo, público, protocolo de aplicação e o instrumento completo no Markdown.

## Ciclo de vida da engenharia de usabilidade

A seção de ciclo de vida está bem encaminhada. A equipe descreve software, hardware, capacidades e restrições da plataforma. As capacidades estão alinhadas às funcionalidades centrais do QuestIA: feedback instantâneo, visualização de dados e monitoramento de qualidade. As restrições também são plausíveis, especialmente dependência de conexão e rigidez de domínio.

A tabela de princípios gerais inclui LGPD, Lei de Acessibilidade, ABNT NBR ISO 9241 e uma norma ética. Isso demonstra preocupação com privacidade, acessibilidade e ergonomia da interação humano-sistema. Em projetos de IHC, princípios gerais de projeto devem transformar conhecimento ergonômico, legal e normativo em critérios para orientar a interface.

As metas qualitativas também estão coerentes: confiança, redução de carga mental e satisfação. Elas refletem problemas reais do projeto, especialmente a necessidade de o usuário confiar na correção automática e compreender seus critérios.

Pontos que precisam ser corrigidos ou complementados:

- As metas quantitativas foram apresentadas como pesos percentuais, mas não como critérios mensuráveis de usabilidade. Em IHC, metas quantitativas precisam indicar valores verificáveis, como “80% dos alunos conseguem submeter uma resposta sem ajuda”, “professores localizam a questão com pior desempenho em até 60 segundos” ou “nota SUS média acima de 75”.
- A tabela usa cinco fatores, o que atende ao requisito de não usar apenas eficácia, eficiência e satisfação. No entanto, os nomes poderiam ser alinhados mais diretamente aos fatores de Nielsen: facilidade de aprendizado, facilidade de recordação, eficiência, segurança no uso/baixa taxa de erros e satisfação.
- A meta “baixa taxa de erros” está conceitualmente adequada, mas precisa especificar erro de quem: erro de uso da interface, erro de interpretação do feedback, erro de calibração da IA ou erro de correção.
- A inclusão da Resolução CNS 196/96 deve ser revisada, pois em muitos contextos ela foi substituída por normativas posteriores. O ponto ético é pertinente, mas convém atualizar a referência normativa usada em pesquisa com seres humanos.

**Recomendação de melhoria:** converter os pesos em indicadores testáveis. Por exemplo: “pelo menos 90% dos professores devem conseguir gerar o relatório de lacunas sem auxílio”; “tempo médio para encontrar a questão com maior erro inferior a 1 minuto”; “máximo de 1 erro crítico por sessão de simulado”.

## Modelo conceitual: cenários de interação, DCC, mapa de objetivos e signos

O modelo conceitual é uma das partes mais ricas do projeto. A equipe apresenta cenários de interação para aluno e professor, tabelas de Design Centrado na Comunicação, mapas de objetivos e uma tabela unificada de signos. A tabela de signos é especialmente positiva, pois reúne origem, observações, tipo de conteúdo, restrição, valor default, prevenção e recuperação. Isso atende bem à exigência de unir as três tabelas conceituais.

Os cenários de interação mostram como o sistema responde às ações do usuário. Isso é adequado porque, diferentemente do cenário de problema, o cenário de interação já descreve a intervenção proposta. A equipe também mantém a coerência com as funcionalidades de feedback, comparação, mapa de calor, discrepância e relatório de lacunas.

O Design Centrado na Comunicação está estruturado como diálogo entre usuário e designer preposto/sistema. Essa é uma boa direção, pois a abordagem semiótica de IHC entende a interface como uma mensagem do designer para o usuário, e a interação como uma conversa mediada por signos.

Pontos que precisam ser corrigidos ou complementados:

- O enunciado pedia destacar em negrito o texto alterado entre cenário de problema e cenário de interação. A equipe usa negrito em várias partes, mas não apresenta uma comparação clara com o cenário de problema original.
- Alguns trechos do cenário de interação incluem detalhes de interface, como “campo abaixo”, “comparativo lado a lado” e “gráfico de evolução”. O cenário de interação deve detalhar ações do usuário e respostas do sistema, mas evitar excesso de widgets e rótulos de interface.
- Na tabela do professor, a fala “O índice de discrepância está em 3%, dentro do limite aceitável” está atribuída ao usuário. Isso parece ser uma fala do sistema. Em DCC, é importante distinguir corretamente as falas do usuário e do designer/sistema.
- Os mapas de objetivos estão referenciados por imagens externas. Não foi possível validar completamente a estrutura visual, embora a existência dos mapas e dos diagramas de consolidação esteja indicada.
- A tabela de signos é forte, mas poderia incluir mais signos ligados a consentimento, privacidade e confiabilidade da IA, como “critério de correção”, “fonte do padrão de resposta”, “confiança da sugestão” e “revisão humana”.

**Recomendação de melhoria:** revisar as falas do DCC e remover elementos excessivamente concretos de interface nos cenários. Em seguida, criar uma versão comparada: trecho do cenário-problema e trecho do cenário-interação, com as alterações em negrito.

## MoLIC

A seção de MoLIC demonstra boa compreensão geral da Engenharia Semiótica: a equipe trata a interface como conversa entre usuário e sistema, apresenta metáforas de interação e define dois contextos: aprendizado orientado para o aluno e gestão estratégica para o professor.

Há dois diagramas referenciados, coerentes com os dois perfis centrais. Também há detalhamento textual das cenas principais, incluindo seleção de contexto, escrita, processamento, entrega de feedback, recuperação e aprofundamento. A presença de tratamento de rupturas, como texto insuficiente e falha de NLP, é um ponto positivo, pois MoLIC deve representar não apenas o caminho ideal, mas também rupturas comunicativas e possibilidades de recuperação.

Pontos que precisam ser corrigidos ou complementados:

- Não foi possível validar visualmente a sintaxe completa dos diagramas, pois as imagens estão em links externos e não foram incluídas no ZIP. Portanto, não foi possível confirmar com segurança se há cenas com inputs/outputs, falas de transição adequadas, fluxos tracejados de recuperação/cancelamento e caixa preta de processamento interno.
- A seção apresenta títulos de diagramas, mas poderia explicitar formalmente “Nome do cenário” antes de cada diagrama, como o modelo solicita.
- O texto menciona “Ruptura Temporária” e “Breakdown”, mas a entrega deveria garantir que esses elementos também aparecem no diagrama, não apenas na explicação.
- A metáfora de “Tutor Particular Especializado” e “Assistente de Auditoria” é útil, mas poderia ser conectada a signos concretos da interface e a decisões de comunicação.

**Recomendação de melhoria:** incluir os arquivos das imagens no repositório ou exportar os diagramas em PNG/SVG localmente. Abaixo de cada diagrama, listar: cenas, falas de transição, signos de input, signos de output, rupturas, recuperação e processamento interno.

## Figma e telas finais

A entrega de telas finais está bem atendida. A equipe inclui link para o protótipo interativo e apresenta telas de input de respostas, feedback da IA, dashboard, métricas de discrepância e histórico de provas corrigidas. As descrições mostram que as telas estão alinhadas aos cenários e tarefas do projeto.

A existência de telas finais de alta fidelidade é suficiente, conforme a regra de correção, mesmo que o projeto não dependesse obrigatoriamente de um link Figma. Nesse caso, a equipe entregou tanto link quanto imagens/descrições.

Pontos que podem melhorar:

- Relacionar cada tela ao respectivo cenário MoLIC. Por exemplo: “Tela X corresponde à cena Y do diagrama do aluno”.
- Indicar quais telas foram alteradas após avaliação heurística ou observação do usuário.
- Incluir todas as imagens localmente no repositório para evitar perda de evidência no futuro.

## Planejamento da avaliação — DECIDE

A tabela DECIDE está completa e conceitualmente correta. A equipe define objetivos, questões de avaliação, métodos, questões práticas, questões éticas e forma de análise. O planejamento está alinhado ao projeto: compreensibilidade do feedback para o aluno, redução da carga mental do professor e avaliação do dashboard.

O uso combinado de inspeção heurística e teste de usabilidade por observação é adequado, pois uma técnica inspeciona problemas por julgamento especializado e a outra observa dificuldades reais de usuários em tarefas.

Pontos que precisam ser corrigidos ou complementados:

- A etapa Choose poderia justificar melhor por que inspeção heurística e observação respondem às perguntas formuladas.
- A etapa Identify cita 3–5 alunos e 2 professores, mas o projeto final de observação parece ter sido executado apenas com professores. Essa inconsistência precisa ser resolvida.
- A lista de instrumentos está correta, mas genérica. O repositório deveria conter os instrumentos completos: TCLE, questionário, tabela de observação e formulário de avaliação heurística.
- A etapa Evaluate poderia indicar métricas exatas: taxa de sucesso, tempo por tarefa, número de erros, tipos de erro, severidade dos problemas, satisfação e recomendações de redesign.

**Recomendação de melhoria:** conectar o planejamento DECIDE diretamente às entregas de heurística e observação. O que foi planejado deve aparecer executado depois.

## Avaliação heurística

A avaliação heurística apresenta pontos positivos: a equipe inclui as dez heurísticas de Nielsen, a escala de severidade, dois problemas identificados com print, heurística violada, grau de severidade, descrição e sugestão de melhoria. Também inclui uma boa prática de visibilidade do status do sistema.

O problema do tamanho excessivo de fonte foi classificado como severidade 1, o que é coerente quando o impacto é principalmente estético. A falta de botão para cancelar submissão foi classificada como severidade 2, também plausível, pois afeta controle e liberdade do usuário, mas não impede completamente o uso.

Pontos que precisam ser corrigidos ou complementados:

- A exigência era uma solução completa por pessoa da equipe e todas as telas do projeto. A entrega não identifica avaliadores por integrante e apresenta apenas dois problemas, o que é pouco para um conjunto de pelo menos cinco telas.
- A inspeção deveria cobrir input de resposta, tela de feedback, dashboard overview, métricas de discrepância e histórico. Isso não aparece de forma sistemática.
- O enunciado orienta “somente violações” na primeira parte. A equipe incluiu uma seção de boas práticas, o que também era solicitado em uma segunda parte, então isso não é problema; porém, a parte de violações ficou insuficiente.
- A boa prática apresenta apenas um exemplo. A regra indica uma solução completa por pessoa; seria recomendável ao menos uma boa prática por integrante ou por heurística selecionada.
- Não há tabela consolidada de violações por tela, heurística, severidade e recomendação.

**Como completar:** cada integrante deve inspecionar todas as telas e registrar violações. Uma tabela mínima deveria conter: avaliador, tela, print, heurística, problema, local do problema, severidade, justificativa da severidade e recomendação de correção.

## Avaliação de usabilidade por observação do usuário

A equipe relata observação com dois professores e registra comentários reais sobre clareza da tela, cores, tamanho de fonte e espaçamento. Esse é um bom começo, pois mostra contato com usuários e uso do feedback para melhoria.

Entretanto, a entrega não atende à estrutura solicitada. Avaliação por observação do usuário exige planejamento, procedimento, tarefas, registro sistemático e resultados mensuráveis. A ideia central é observar a interação real, não apenas coletar opinião geral. Por isso, é necessário registrar o que o usuário tentou fazer, onde hesitou, que erros cometeu, quanto tempo levou, se completou a tarefa e qual foi sua satisfação.

Pontos que precisam ser corrigidos ou complementados:

- Falta o fluxograma de avaliação de usabilidade por observação.
- Falta a descrição do procedimento de preparação do teste: convite, ambiente, instruções, termo de consentimento, papel do observador, gravação, início e fim da sessão.
- A lista de tarefas aparece, mas os resultados observados não estão organizados por tarefa.
- A equipe propôs uma tarefa de aluno, mas os usuários relatados são professores. Falta observação com pelo menos um usuário representando o perfil de aluno.
- Falta tabela com grau de sucesso, total de erros, tipos de erros, tempo necessário e grau de satisfação.
- Faltam links dos vídeos, respostas do formulário do usuário e evidências de aplicação.
- As conclusões são muito gerais e não distinguem achados por usuário, tarefa ou tela.

**Recomendação de melhoria:** refazer a seção usando uma tabela por usuário e tarefa. Para cada tarefa, registrar sucesso, erros, tipo de erro, tempo, comentário espontâneo e recomendação de redesign. Isso aproximaria a entrega do método solicitado e permitiria justificar as alterações feitas no protótipo.

## Falhas de alinhamento entre entregas

O projeto mantém boa coerência temática, mas há alguns desalinhamentos que devem ser ajustados:

- O planejamento DECIDE prevê 3–5 alunos e 2 professores, mas a observação documentada apresenta apenas dois professores.
- A coleta de dados fala em questionários para aluno e professor, mas os instrumentos completos não aparecem no Markdown, apenas links.
- A análise heurística aponta problemas de telas, mas não fica claro se essas correções foram incorporadas nas telas finais do Figma.
- O cenário de problema do professor já usa o QuestIA; depois, o cenário de interação também usa o QuestIA. Isso reduz a diferença entre problema e solução.
- Os diagramas e telas estão principalmente como imagens externas. Para fins de avaliação acadêmica, o repositório deveria conter os arquivos de evidência localmente.

## Pontos fortes a preservar

- Tema relevante e bem delimitado no domínio educacional.
- Dois perfis de usuário bem escolhidos e mantidos ao longo do projeto.
- Funcionalidades coerentes com os problemas levantados: feedback instantâneo, comparação com referência, métricas de discrepância, mapa de calor, histórico e relatório de lacunas.
- Boa preocupação com explicabilidade da IA, especialmente ao mostrar por que a resposta foi avaliada de determinada forma.
- Protótipos e telas finais sugerem maturidade visual acima do mínimo esperado.
- Tabela de signos do modelo conceitual está bem estruturada e integrada.
- Uso de MoLIC e DCC de forma compatível com a ideia de interface como comunicação.
- Planejamento DECIDE bem organizado.

## Pontos de maior prioridade para correção

| Prioridade | Item | O que corrigir primeiro |
|---:|---|---|
| Alta | Coleta de dados | Incluir aspectos éticos, “que dados/de quem coletar”, três técnicas diferentes e instrumentos completos. |
| Alta | Observação do usuário | Incluir fluxograma, protocolo, tabela por tarefa, tempos, erros, satisfação, vídeos/respostas e pelo menos um usuário aluno. |
| Alta | Avaliação heurística | Avaliar todas as telas, identificar avaliador/integrante, registrar mais violações e consolidar severidade. |
| Alta | Cenário de problema do professor | Remover QuestIA da narrativa de problema e descrever a situação atual sem solução. |
| Média | Análise de concorrência | Explicitar padrões/tendências de mercado e análise de UX/opiniões. |
| Média | Personas e empatia | Inserir fotos, ganhos no mapa de empatia e dados que o sistema deve guardar. |
| Média | Metas quantitativas | Converter pesos percentuais em metas mensuráveis. |
| Média | Evidências visuais | Incluir imagens e diagramas localmente no repositório. |
| Baixa | Padronização | Ajustar títulos, campos formais, autoria e status para ficar mais próximo dos modelos. |

## Parecer final

O QuestIA é um projeto promissor e conceitualmente coerente. A equipe demonstra domínio razoável do problema, boa sensibilidade para necessidades de professores e alunos e capacidade de transformar essas necessidades em funcionalidades de interface. As telas e o modelo conceitual indicam maturidade de design.

Apesar disso, a entrega ainda não atinge plenamente o padrão exigido nas vídeos-aulas porque várias atividades foram entregues de forma resumida ou incompleta. O principal problema não é a ideia do produto, mas a falta de rigor metodológico em algumas técnicas de IHC. Em especial, coleta de dados, avaliação heurística e observação do usuário precisam ser tratadas como métodos formais, com protocolo, instrumento, execução, evidência e análise.

Com as correções indicadas, o projeto pode evoluir bastante. A recomendação central é transformar as boas ideias já existentes em documentação verificável: perguntas completas, instrumentos completos, diagramas locais, tabelas de análise e resultados sistemáticos. Isso tornará o trabalho mais forte tanto como projeto de interface quanto como exercício acadêmico de IHC.

## Base conceitual usada na avaliação

- Barbosa, S. D. J.; Silva, B. S. *Interação Humano-Computador*. Elsevier, 2010.
- Preece, J.; Rogers, Y.; Sharp, H. *Interaction Design: Beyond Human-Computer Interaction*. Wiley.
- Nielsen, J. *Usability Engineering*. Morgan Kaufmann, 1993.
- Nielsen, J.; Molich, R. Heuristic evaluation of user interfaces.
- ISO 9241-11: ergonomia da interação humano-sistema — usabilidade como eficácia, eficiência e satisfação em contexto de uso.
- ISO 9241-210: processo de design centrado no humano para sistemas interativos.
