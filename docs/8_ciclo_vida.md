**CICLO DE VIDA DE ENGENHARIA DE USABILIDADE**

1. **Características da Plataforma**  
   

| Característica | Descrição |
| :---- | :---- |
| Descrição do Software | Interface web para interação com algoritmo de correção automática de questões dissertativas do ENADE, utilizando tecnologias como Python, Node e bibliotecas de NLP. |
| Descrição do Hardware | Estações de trabalho (Desktops/Laptops) para professores em ambiente profissional e dispositivos diversos (Laptops/Tablets) para alunos em ambiente doméstico ou escolar. |
| LISTA DE Capacidades da Plataforma (com explicação) | 1. Feedback Instantâneo: Retorno em tempo real após submissão. <br> 2. Visualização de Dados: Geração de mapas de calor e gráficos de evolução. <br> 3. Monitoramento de Qualidade: Alertas automáticos de discrepância e fadiga. |
| LISTA DE Restrições da Plataforma (com explicação) | 1. Dependência de Conexão: Necessita de internet estável para o processamento remoto do modelo de linguagem. <br> 2. Rigidez de Domínio: O algoritmo é treinado especificamente para o padrão de resposta da banca do ENADE. |

2. **Princípios Gerais do Projeto (INCREMENTAR TABELA)**     

| Nome | Descrição | Link |
| :---- | :---- | :---- |
| Descrição do Contexto | Ambiente acadêmico de alta pressão (preparação para o ENADE), onde a rapidez no feedback e a precisão da nota são críticas para o aprendizado do aluno e gestão do professor. |  |
| Lei Geral de Proteção de Dados (LGPD) \- Lei n.º 13.709/2018 | Fundamental para proteger as respostas dissertativas e dados de desempenho de alunos e professores. | [https://www.planalto.gov.br/ccivil\_03/\_ato2015-2018/2018/lei/l13709.htm](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) |
| Lei n.º 10.098/2000 \- Lei da Acessibilidade |  Garante que a interface de correção e os simulados sejam acessíveis a todos os estudantes. | [https://www.planalto.gov.br/ccivil\_03/leis/l10098.htm](https://www.planalto.gov.br/ccivil_03/leis/l10098.htm) |
| ABNT NBR ISO 9241 Ergonomia da interação humano-sistema |  Orienta o design centrado no humano, focando na clareza dos dashboards estratégicos e facilidade de leitura do feedback. | [https://www.inf.ufsc.br/\~edla.ramos/ine5624/\_Walter/Normas/Parte%2011/iso9241-11F2.pdf](https://www.inf.ufsc.br/~edla.ramos/ine5624/_Walter/Normas/Parte%2011/iso9241-11F2.pdf) |
| Resolução nº 196/96 - Ética em Pesquisa com Seres Humanos | Garante os princípios de não maleficência, autonomia e beneficência. É vital para o QuestIA, pois o projeto lida com alunos e subordinados (vulneráveis), exigindo consentimento livre e esclarecido | [https://bvsms.saude.gov.br/bvs/saudelegis/cns/1996/res0196_10_10_1996.html](https://bvsms.saude.gov.br/bvs/saudelegis/cns/1996/res0196_10_10_1996.html)  |
   

3. **Metas de Usabilidade**

   1. **Qualitativo**
      - **Confiança:** O aluno deve sentir que a correção automática é justa e coerente com o padrão oficial da banca.

      - **Redução de Carga Mental:** O professor deve conseguir identificar lacunas de aprendizado da turma sem precisar tabular dados manualmente.

      - **Satisfação:** A interface deve ser clara o suficiente para que alunos com pouca familiaridade tecnológica consigam realizar simulados sem suporte externo.


   3. **Quantitativo**  
    
| Metas | Porcentagem | Justificativa |
| ----- | :---- | :---- |
| Eficiência | 20% | Meta principal para o professor: diminuir pela metade o tempo gasto em correções manuais através da automação por IA. |
| Aprendizado | 20% | O aluno deve ser capaz de realizar e submeter seu primeiro simulado sem consultar manuais ou suporte externo. |
| Memorização | 20% | O usuário (aluno) deve lembrar como navegar pelos simulados mesmo após longos períodos sem estudar, dada a sazonalidade do ENADE. |
| Baixa taxa de erros | 20% | Garantir que a diferença entre a nota da IA e o padrão de resposta oficial seja mínima para manter a credibilidade do sistema. |
| Satisfação do usuário | 20% | Atingir um alto índice de satisfação subjetiva, reduzindo a ansiedade do aluno e a fadiga do corretor humano. |
| **Total** | **100%** |  |