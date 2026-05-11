# Diagramas MoLIC - QuestIA

Abaixo estão os diagramas MoLIC gerados em formato Mermaid.js, modelados de acordo com a sintaxe oficial (Barbosa e Silva, 2010).

Você pode visualizar estes diagramas copiando e colando os blocos de código no [Mermaid Live Editor](https://mermaid.live/).

## 1. Ciclo de Feedback do Aluno (Praticar Simulado)

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

## 2. Dashboard Estratégico (Professor)

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