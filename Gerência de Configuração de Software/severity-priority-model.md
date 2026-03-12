# Modelo de Severidade e Prioridade

Este documento define o modelo de classificação de **severidade** e **prioridade** utilizado no projeto. O objetivo é ajudar a equipe a identificar a gravidade dos problemas e organizar a ordem de resolução das issues do repositório.

---

# Severidade do projeto

A severidade representa o **impacto de um problema no funcionamento do sistema**. Essa classificação ajuda a equipe a entender o quão grave é uma falha e qual o seu impacto para os usuários.

O grau de severidade é um conceito importante para avaliar a gravidade dos problemas, guiando a equipe para que aplique os recursos de forma eficiente e priorize corretamente as correções.

## Critérios de Severidade

| Severidade | Descrição |
|-----|-----|
| **Critical** | defeito que bloqueia completamente o uso do sistema |
| **Major** | funcionalidade principal que não funciona conforme esperado |
| **Minor** | problema que afeta parcialmente uma funcionalidade |
| **Enhancement** | melhoria estética ou pequena melhoria de interface |

### Descrição das categorias

**Critical**

Um defeito que impede o funcionamento do sistema ou de uma funcionalidade essencial.

Exemplos:
- o sistema não permite registrar atividades físicas ou domésticas
- o aplicativo trava ao salvar uma atividade
- o usuário não consegue acessar sua conta

---

**Major**

Problema em uma funcionalidade principal que não atende aos requisitos esperados.

Exemplos:
- atividades registradas não aparecem no histórico
- o sistema salva informações incorretas sobre as atividades
- o relatório de atividades apresenta dados inconsistentes

---

**Minor**

Problema que afeta parcialmente uma funcionalidade, mas não impede o uso do sistema.

Exemplos:
- problema na ordenação do histórico de atividades
- erro na exibição de atividades registradas
- falha na atualização automática da lista de atividades

---

**Enhancement**

Melhoria estética ou ajuste menor que não afeta a funcionalidade principal do sistema.

Exemplos:
- correção de textos na interface
- melhoria na organização da tela de registro
- ajustes visuais no layout das páginas

---

## Tomada de decisão

Esse modelo de classificação de severidade foi escolhido porque permite categorizar diferentes tipos de problemas, desde falhas críticas até melhorias estéticas. Dessa forma, a equipe consegue identificar rapidamente os problemas mais graves e direcionar os esforços para as correções mais importantes.

---

## Aplicação

Os níveis de severidade serão aplicados às **issues do repositório do projeto**, permitindo que a equipe identifique rapidamente a gravidade de cada problema e priorize as correções mais críticas.

---

# Prioridade do projeto

A prioridade define **a ordem em que as tarefas devem ser resolvidas**. Ela considera tanto a necessidade da alteração quanto a urgência da sua implementação.

Para isso, utiliza-se um modelo baseado em duas dimensões:

- **necessidade**
- **urgência**

Cada dimensão recebe uma pontuação de **1 a 4**, sendo 4 o valor mais alto.

A soma dessas pontuações gera a **criticidade da issue**, que define sua prioridade de execução.

---

# Critérios de Prioridade

A priorização foi dividida em classificações representadas por notas para as categorias de **necessidade** e **urgência** dos problemas e funcionalidades envolvidos na aplicação.

A soma das notas atribuídas a cada issue fornece uma pontuação que reflete sua criticidade. Quanto maior a pontuação, maior a prioridade da issue.

![Modelo de prioridade e severidade](https://github.com/Artrite-Fit/docs/raw/docs/config-management/Ger%C3%AAncia%20de%20Configura%C3%A7%C3%A3o%20de%20Software/images/modelo-de-prioridade-e-severidade.png)

---

## Necessidade

Representa o nível de importância da mudança para o funcionamento ou evolução do sistema.

| Classificação | Descrição |
|-----|-----|
| **Extremamente necessário (4)** | problema crítico ou funcionalidade essencial |
| **Necessário (3)** | funcionalidade importante para o sistema |
| **Otimização (2)** | melhoria que otimiza o sistema ou experiência |
| **Incremento (1)** | melhoria pequena ou cosmética |

### Exemplos

- impossibilidade de registrar atividades → **Extremamente necessário**
- necessidade de adicionar nova categoria de atividade → **Necessário**
- melhoria no desempenho do carregamento do histórico → **Otimização**
- melhoria visual na interface → **Incremento**

---

## Urgência

Representa o tempo necessário para resolver a issue.

| Classificação | Descrição |
|-----|-----|
| **Urgente (4)** | requer ação imediata |
| **Assim que possível (3)** | importante, mas pode aguardar um pouco |
| **Pouco urgente (2)** | pode ser resolvido em prazo maior |
| **Pode esperar (1)** | baixa urgência |

---

## Criticidade

A criticidade é calculada pela soma das notas de **necessidade** e **urgência**.

```
criticidade = necessidade + urgência
```

Quanto maior a pontuação, maior a prioridade da issue.

Exemplo:

- necessidade: 4  
- urgência: 3  

criticidade total = **7**

Isso indica que essa issue deve ser tratada antes de outra com pontuação menor.

---

## Tomada de decisão

Esse modelo foi escolhido porque permite avaliar tanto a importância quanto a urgência das tarefas. Dessa forma, a equipe pode tomar decisões mais informadas sobre quais issues devem ser resolvidas primeiro.

---

## Aplicação

As classificações de **severidade** e **prioridade** serão aplicadas às issues do repositório do projeto.

Isso permitirá que a equipe tenha uma visão clara sobre:

- gravidade dos problemas
- importância das funcionalidades
- ordem de implementação das tarefas

---

## Exemplos

Alguns exemplos aplicados ao sistema:

- impossibilidade de registrar atividades físicas ou domésticas → **Extremamente necessário + Urgente**
- erro na exibição do histórico de atividades → **Necessário + Assim que possível**
- melhoria na organização do relatório de atividades → **Otimização + Pouco urgente**
- correção de textos na interface → **Incremento + Pode esperar**

![Exemplos de problemas e funcionalidades](https://github.com/Artrite-Fit/docs/raw/docs/config-management/Ger%C3%AAncia%20de%20Configura%C3%A7%C3%A3o%20de%20Software/images/problema-funcionalidade.png)
