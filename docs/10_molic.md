# MOLIC (Modelagem da Linguagem de Interação e Comunicação)

A MOLIC trata a interface como uma conversa entre o designer (através do sistema) e o usuário. Para o QuestIA, essa conversa é dividida em dois grandes contextos: o de **Aprendizado Orientado** (Aluno) e o de **Gestão Estratégica** (Professor).

## 1. Metáforas de Interação
*   **Para o Aluno:** O sistema atua como um **"Tutor Particular Especializado"**. Ele não apenas dá a nota, mas explica o critério e orienta o estudo, como um professor faria em uma sessão de monitoria.
*   **Para o Professor:** O sistema atua como um **"Assistente de Auditoria"**. Ele processa o volume massivo de dados e "cutuca" o professor sobre inconsistências ou cansaço, garantindo a qualidade do trabalho humano.

## 2. Diagramas de Interação (MoLIC)

Os diagramas abaixo foram modelados seguindo a sintaxe oficial (Barbosa e Silva, 2010), tratando a interface como uma conversa direcionada a objetivos.

### Diagrama 1: O Ciclo de Feedback do Aluno (Praticar Simulado)
Esta cena descreve o diálogo central de submissão e correção.

```mermaid
graph TD
    %% Entry Point (Ubiquitous Access)
    Start(( )) -->|u: quero treinar para o ENADE<br/>gco: Praticar Simulado| SelectScene

    %% Scene: Select Question
    subgraph SelectScene [Cena: Selecionar Questão]
        direction TB
        S1[d+u: tema, ano, questão]
    end

    SelectScene -->|u: selecionar questão X| WorkScene

    %% Scene: Redigir Resposta
    subgraph WorkScene [Cena: Redigir Resposta]
        direction TB
        W1[d: enunciado da questão<br/>d+u: campo de texto rascunho]
    end

    WorkScene -->|u: solicitar correção| ProcessNode{ }
    
    %% Processing & Breakdowns
    ProcessNode -->|precond: resposta curta<br/>[TA] d: resposta incompleta| WorkScene
    ProcessNode -->|d: processando...| FeedbackScene

    %% Scene: Avaliar Desempenho
    subgraph FeedbackScene [Cena: Avaliar Desempenho]
        direction TB
        F1[d: nota estimada, justificativa<br/>d+u: termos encontrados/faltantes]
    end

    FeedbackScene -->|u: não entendi meu erro| CompareScene
    FeedbackScene -->|u: terminar sessão<br/>gcc: Praticar Simulado| EndNode(( ))

    %% Scene: Comparativo Lado a Lado (Breakdown Recovery)
    subgraph CompareScene [Cena: Comparativo Lado a Lado]
        direction TB
        C1[d: resposta do aluno vs padrão oficial]
    end

    CompareScene -->|u: ok, entendi| FeedbackScene
    CompareScene -->|u: quero tentar novamente| WorkScene
```
*(Caso a imagem não carregue, cole o código acima no [Mermaid Live Editor](https://mermaid.live/))*

### Diagrama 2: A Gestão de Qualidade do Professor
Esta cena foca na supervisão das correções e saúde do docente.

```mermaid
graph TD
    %% Entry Point
    Start(( )) -->|u: ver desempenho da turma<br/>gco: Analisar Correções| DashboardScene

    %% Scene: Dashboard Overview
    subgraph DashboardScene [Cena: Dashboard Geral]
        direction TB
        D1[d: notas, média, engajamento<br/>d+u: filtros por turma/tema]
    end

    DashboardScene -->|u: ver detalhes da questão X| HeatmapScene
    DashboardScene -->|u: sair<br/>gcc: Analisar Correções| EndNode(( ))

    %% Scene: Análise de Lacunas (Mapa de Calor)
    subgraph HeatmapScene [Cena: Mapa de Calor]
        direction TB
        H1[d: pontos fracos da turma<br/>d+u: termos técnicos mais errados]
    end

    HeatmapScene -->|u: voltar| DashboardScene
    HeatmapScene -->|precond: tempo de correção rápido demais<br/>[SR] d: alerta de fadiga| FatigueNode{ }

    %% Fatigue Intervention
    FatigueNode -->|d: você parece cansado, deseja pausar?| FatigueScene

    subgraph FatigueScene [Cena: Intervenção de Fadiga]
        direction TB
        F1[d: aviso sobre consistência das notas]
    end

    FatigueScene -->|u: sim, pausar| PauseNode(( ))
    FatigueScene -->|u: não, continuar| CalibrationScene

    HeatmapScene -->|u: revisar notas da questão| CalibrationScene

    %% Scene: Histórico e Calibragem
    subgraph CalibrationScene [Cena: Histórico de Respostas]
        direction TB
        C1[d: lista de alunos e notas<br/>d+u: aceitar nota da IA ou reavaliar]
    end

    CalibrationScene -->|u: confirmar revisões| ProcessNode{ }
    
    ProcessNode -->|d: revisões salvas| DashboardScene
```
*(Caso a imagem não carregue, cole o código acima no [Mermaid Live Editor](https://mermaid.live/))*

### Detalhamento das Cenas Principais

**Cena A: Fluxo do Aluno**
Esta cena descreve o diálogo central de submissão e correção.

1.  **Abertura:** Usuário acessa e o sistema pergunta o objetivo ("O que vamos revisar hoje?").
2.  **Seleção de Contexto:** Usuário escolhe a questão. O sistema apresenta o enunciado e o "contrato" (tempo sugerido e critérios).
3.  **Turno de Escrita:** O usuário redige. O sistema oferece suporte passivo (autosave) para evitar perda de progresso (Prevenção de Erro).
4.  **Processamento (Ruptura Temporária):** O usuário solicita correção. O sistema sinaliza que está "pensando" (Visibilidade do Status).
5.  **Entrega do Feedback:** O sistema apresenta a nota e a justificativa.
    *   *Sinal Conversacional:* "Sua nota foi X porque você esqueceu o conceito Y."
6.  **Recuperação e Aprofundamento (Breakdown):** Se o usuário não entende, ele solicita o "Lado a Lado". O sistema abre a visão comparativa.

### Cena B: A Gestão de Qualidade do Professor
Esta cena foca na supervisão das correções e saúde do docente.

1.  **Abertura Estratégica:** O sistema apresenta o panorama geral ("Aqui está o resumo da sua turma").
2.  **Análise de Padrões:** O professor interage com o Mapa de Calor. O sistema revela: "A Questão 3 é o seu maior gargalo atual".
3.  **Monitoramento de Fadiga (Intervenção do Sistema):**
    *   *Sistema:* "Notei que seu tempo de correção caiu. Você parece cansado. Quer fazer uma pausa?"
    *   *Professor:* Pode aceitar a sugestão ou continuar (Controle do Usuário).
4.  **Ajuste de Calibragem:** O professor analisa as métricas de discrepância e decide se a IA precisa ser mais flexível ou rígida.

## 3. Signos e Expressões do Sistema

| Signo | Significado Conversacional |
| :--- | :--- |
| **Destaque Verde** | "Isso mesmo! Você acertou este ponto técnico." |
| **Destaque Vermelho** | "Atenção: este termo era esperado pela banca e não foi encontrado." |
| **Alerta de Discrepância** | "Cuidado: há uma divergência incomum entre o padrão e as notas atuais." |
| **Indicador de Processamento** | "Espere um pouco, estou lendo seu texto cuidadosamente..." |

## 4. Tratamento de Rupturas (Error Recovery)

*   **Texto Insuficiente:** Se o aluno envia uma resposta muito curta, o sistema não apenas dá nota baixa, mas sugere: "Sua resposta parece incompleta. Tente elaborar mais sobre [Termo X]".
*   **Falha de NLP:** Se o algoritmo não consegue processar um sinônimo novo, o professor tem o poder de "Ensinar o Sistema", validando aquele termo para futuras correções.


