# Etapa 4 - APRENDIZAGEM DE MÁQUINA

Nesta etapa, os dados previamente tratados serão utilizados na aplicação de algoritmos de aprendizagem de máquina, com foco na identificação de padrões e possíveis anomalias nas transações analisadas. Serão realizados experimentos com diferentes modelos, permitindo comparar seus desempenhos e selecionar a abordagem mais adequada ao problema proposto, considerando sua capacidade de gerar resultados consistentes e apoiar a análise do cenário.

**Link para o arquivo de aprendizagem de máquina**: [Aprendizado de máquina](creditcard_aprendizagem_de_maquina.ipynb)

# Etapa 4 - Aprendizado de Máquina

## Visão Geral

Nesta etapa do projeto, foram realizados experimentos com algoritmos de aprendizado de máquina aplicados ao problema de **detecção de fraude em cartões de crédito**.

O objetivo foi avaliar a capacidade de diferentes modelos em classificar transações como **fraudulentas ou legítimas**, considerando não apenas a acurácia, mas também o **tempo de treinamento** e o **tempo de predição**. Em sistemas financeiros, esses fatores são fundamentais, já que a identificação rápida de uma fraude pode evitar prejuízos para empresas e consumidores.

---

## Objetivo

O principal objetivo desta etapa foi comparar diferentes algoritmos de classificação para identificar qual deles apresenta melhor desempenho no contexto do projeto.

Foram analisados os seguintes aspectos:

- capacidade de classificar corretamente as transações;
- eficiência computacional;
- equilíbrio entre desempenho e tempo de resposta.

---

## Modelos Testados

### Decision Tree (Árvore de Decisão)

A **Decision Tree** é um algoritmo supervisionado que organiza as decisões em formato de árvore, realizando divisões sucessivas nos dados até chegar a uma classificação final.

Uma das suas principais vantagens é a facilidade de interpretação, pois permite visualizar de forma clara quais critérios levaram o modelo a decidir se uma transação é fraudulenta ou não.

#### Resultados

- **Acurácia:** 0.9576442774715307
- **Tempo de treinamento:** 15.39626641399991 segundos
- **Tempo de predição:** 0.014682965999782027 segundos

#### Análise

A Decision Tree apresentou desempenho satisfatório e um tempo de predição bastante rápido. No entanto, sua acurácia foi inferior à dos modelos mais robustos testados. Mesmo assim, continua sendo uma boa opção quando se busca simplicidade e interpretabilidade.

---

### Random Forest

O **Random Forest** é um algoritmo baseado em várias árvores de decisão. Em vez de depender de uma única árvore, ele combina o resultado de diversas árvores para chegar a uma decisão final mais estável.

Esse método costuma reduzir problemas de overfitting e, em muitos casos, apresenta melhor capacidade preditiva.

#### Resultados

- **Acurácia:** 0.9994967405170698
- **Tempo de treinamento:** 403.08355298400033 segundos
- **Tempo de predição:** 0.8259190950002449 segundos

#### Análise

O Random Forest foi o modelo que apresentou **melhor acurácia** entre os algoritmos analisados. Em compensação, exigiu um tempo de treinamento significativamente maior. Portanto, é um modelo extremamente preciso, mas com custo computacional mais elevado.

---

### SVC (Support Vector Classification)

O **SVC** busca encontrar um limite de separação ideal entre as classes, maximizando a distância entre os grupos.

Como o problema de fraude é um caso de classificação binária (fraude ou não fraude), esse algoritmo se mostrou bastante adequado.

#### Resultados

- **Acurácia:** 0.9798930281006051
- **Tempo de treinamento:** 2.2176099250000334 segundos
- **Tempo de predição:** 0.010460080000029848 segundos

#### Análise

O SVC apresentou um bom equilíbrio entre desempenho e velocidade. Embora sua acurácia tenha sido menor que a do Random Forest, o tempo de treinamento e predição foi bem menor, o que pode ser vantajoso em aplicações que exigem respostas rápidas.

---

### KNN (K-Nearest Neighbors)

O **KNN** classifica uma nova observação com base nos exemplos mais próximos do conjunto de dados.

É um algoritmo simples e eficiente em alguns cenários, mas geralmente exige mais processamento na etapa de predição.

#### Resultados

- **Acurácia:** 0.9991573329588147
- **Tempo de treinamento:** 0.05537654799991287 segundos
- **Tempo de predição:** 216.95716825099953 segundos

#### Análise

O KNN apresentou ótima acurácia e treinamento extremamente rápido. No entanto, o tempo de predição foi muito alto, o que o torna pouco indicado para sistemas de detecção de fraude em tempo real.

---

## Outros Modelos Avaliados

Além dos modelos descritos acima, também foram realizados testes com outros algoritmos.

| Modelo | Precisão | Recall | F1-Score | Acurácia | Tempo Treino (s) | Tempo Predição (s) |
|--------|---------:|-------:|---------:|---------:|-----------------:|-------------------:|
| Logistic Regression | 0.998353 | 0.993504 | 0.995554 | 0.993504 | 2.503713 | 0.016222 |
| MLP (Multi-layer Perceptron) | 0.999307 | 0.999309 | 0.999308 | 0.999309 | 179.962757 | 0.294605 |
| Gradient Boosting | 0.999265 | 0.999263 | 0.999264 | 0.999263 | 886.039815 | 0.167188 |
| XGBoosting | 0.998350 | 0.994277 | 0.995982 | 0.994277 | 6.386699 | 0.201516 |

Esses testes ajudaram a ampliar a comparação entre diferentes abordagens de classificação supervisionada.

---

## Considerações Finais

Com base nos experimentos realizados, observou-se que o **Random Forest** apresentou o melhor resultado em termos de acurácia, tornando-se o modelo com maior capacidade de identificar corretamente transações fraudulentas.

Por outro lado, quando o foco é velocidade de processamento, o **SVC** se mostrou uma alternativa interessante, apresentando boa acurácia com menor custo computacional.

Dessa forma, a escolha do modelo depende do objetivo principal do sistema:

- **Maior precisão:** Random Forest
- **Maior velocidade:** SVC

No contexto deste projeto, em que a identificação correta de fraudes é um fator crítico, o **Random Forest** se destacou como o modelo com melhor desempenho geral.
