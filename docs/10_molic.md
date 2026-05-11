# MOLIC

A MOLIC (Modelagem da Linguagem de Interação e Comunicação) é uma técnica de modelagem que visa representar a interação entre o usuário e o sistema através de diagramas, tratando a interface como uma conversa.

## Diagrama MOLIC

![Diagrama MOLIC QuestIA](https://user-images.githubusercontent.com/12345678/molic-questia.png)

*Nota: O diagrama acima representa os caminhos de diálogo entre o Aluno/Professor e o Sistema de Apoio à Decisão (IA).*

## Descrição dos principais elementos do diagrama

Com base no modelo conceitual de comunicação, os principais elementos do diálogo são:

1. **Abertura e Seleção (Usuário -> Sistema):**
   - O usuário (Aluno ou Professor) inicia a conversa expressando a intenção de praticar ou analisar.
   - O sistema responde oferecendo opções de temas ou turmas.

2. **Processamento de Resposta (Interação Principal):**
   - **Aluno:** Envia o texto técnico. O sistema confirma o recebimento e inicia a análise ("Estou analisando seu texto com base nos critérios oficiais...").
   - **Professor:** Solicita visualização estratégica. O sistema apresenta o mapa de calor e alertas de consistência.

3. **Feedback e Ruptura (Sistema -> Usuário):**
   - O sistema fornece a nota e as lacunas ("Sua nota estimada é 8,5... você esqueceu de citar...").
   - **Recuperação de Erro:** Se o aluno questiona ("Onde exatamente eu errei?"), o sistema entra em um sub-diálogo de comparação detalhada (lado a lado).

4. **Fechamento e Evolução:**
   - O diálogo termina com a validação do aprendizado ou da estratégia de ensino.
   - O sistema oferece dados históricos para consolidar a evolução do usuário no tempo.

5. **Signos de Interface:**
   - **Verde/Vermelho:** Signos visuais que comunicam acerto/erro sem necessidade de texto longo.
   - **Alertas de Fadiga:** Signos proativos do sistema para cuidar do bem-estar do professor.

