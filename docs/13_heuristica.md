# 1) Avaliação de IHC através de inspeção HEURÍSTICA

**Descrição da avaliação**

Avaliação heurística, definida por Nielsen e Molich (1994), é um método de avaliação de usabilidade onde um avaliador procura problemas de usabilidade numa interface com o usuário através da análise e interpretação de um conjunto de princípios ou heurísticas. Este método de avaliação é baseado no julgamento do avaliador.

**Tabela 1 - Conjunto de heurísticas de Nielsen (1994)**

| ID | Heurística | Descrição |
| :---: | :--- | :--- |
| 1 | **Visibilidade do status do sistema** | O sistema deve sempre manter os usuários informados sobre o que está acontecendo através de feedback apropriado, em um tempo razoável. |
| 2 | **Compatibilidade entre sistema e mundo real** | O sistema deve utilizar a linguagem do usuário, com palavras, frases e conceitos familiares para ele. Seguir convenções do mundo real, fazendo com que a informação apareça em uma ordem lógica e natural. |
| 3 | **Controle e liberdade para o usuário** | Suporte a "saídas de emergência" (undo/redo) para quando usuários escolhem funções por engano. |
| 4 | **Consistência e padrões** | Usuários não devem ter que adivinhar se diferentes palavras, situações ou ações significam a mesma coisa. |
| 5 | **Prevenção de erros** | Melhor que uma boa mensagem de erro é um design que previne o problema de acontecer. |
| 6 | **Reconhecimento em lugar de lembrança** | Minimizar a carga de memória do usuário tornando objetos, ações e opções visíveis. |
| 7 | **Flexibilidade e eficiência de uso** | Aceleradores (atalhos) para usuários experientes, permitindo que o sistema atenda a ambos os perfis. |
| 8 | **Projeto minimalista e estético** | Diálogos não devem conter informações irrelevantes ou raramente necessárias. |
| 9 | **Auxiliar os usuários a reconhecer, diagnosticar e recuperar erros** | Mensagens de erro devem ser expressas em linguagem natural, indicar o problema e sugerir uma solução. |
| 10 | **Ajuda e documentação** | Informações fáceis de encontrar, centradas na tarefa e com passos concretos. |

**Tabela 2 - Grau de severidade dos problemas de usabilidade**

| Grau | Tipo | Descrição |
| :---: | :--- | :--- |
| 0 | Sem importância | Não afeta a operação da interface. |
| 1 | Cosmético | Não há necessidade imediata de solução. |
| 2 | Simples | Problema de baixa prioridade (pode ser reparado). |
| 3 | Grave | Problema de alta prioridade (deve ser reparado). |
| 4 | Catastrófico | Muito grave, deve ser reparado de qualquer forma. |

---

## Relato de Violações Encontradas

### Problema 1: Tamanho de fonte excessivo no feedback
![Screenshot 2026-04-08 at 19 54 08](https://github.com/user-attachments/assets/d9354f38-24ba-4ab8-be63-841ce4c760b5)

| Heurística Violada | Grau de Severidade | Descrição do Problema | Sugestão de Melhoria |
| :--- | :---: | :--- | :--- |
| 8. Projeto minimalista e estético | 1 (Cosmético) | A fonte utilizada para o texto de feedback era excessivamente grande, causando poluição visual e exigindo rolagem desnecessária. | Reduzir o tamanho da tipografia para padrões de leitura web (16px a 18px). |

### Problema 2: Falta de botão para cancelar submissão
![Input de Respostas](https://github.com/user-attachments/assets/771b047a-863e-4883-ac0f-3fc40a71a518)

| Heurística Violada | Grau de Severidade | Descrição do Problema | Sugestão de Melhoria |
| :--- | :---: | :--- | :--- |
| 3. Controle e liberdade para o usuário | 2 (Simples) | Uma vez que o aluno inicia a questão, não há um botão claro de "Desistir" ou "Voltar" sem submeter. | Incluir um botão de "Voltar" que salve o rascunho ou cancele a sessão. |

---

# 2) INDICAÇÃO DE BOAS PRÁTICAS DE HEURÍSTICA - HEURÍSTICAS NÃO VIOLADAS

**Exemplo de atendimento de heurística no QuestIA:**

### Heurística 1: Visibilidade do status do sistema
![Feedback IA](https://github.com/user-attachments/assets/b618c376-c29f-4839-a8bb-43a7558e9d31)

**Descrição:** Após clicar em "Solicitar Correção", o sistema exibe imediatamente um indicador de processamento ("Analisando sua resposta...") e, em seguida, apresenta a nota de forma clara. Isso garante que o usuário saiba que sua ação foi recebida e está sendo processada, cumprindo o requisito de feedback em tempo razoável.
