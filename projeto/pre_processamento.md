# Etapa 3 - PRÉ-PROCESSAMENTO DE DADOS

## Visão Geral
Nesta etapa, utilizando a linguagem Python, é realizado o pré-processamento dos dados com o objetivo de prepará-los para análises mais precisas e confiáveis. Esse processo envolve a limpeza, transformação e organização dos dados brutos, garantindo maior qualidade e consistência das informações para futuras análises e para o treinamento de modelos de machine learning.

**Tratamento Básico dos Dados:**

Durante essa fase, são aplicadas técnicas como tratamento de valores ausentes, remoção de duplicidades, padronização de formatos e normalização dos dados. Além disso, são gerados gráficos exploratórios que auxiliam na visualização dos dados, permitindo identificar padrões, tendências, outliers e possíveis inconsistências.

## Ferramentas Utilizadas
- **Bibliotecas de Manipulação de dados:** Responsável por carregar, limpar e transformar os dados. Numpy e Pandas
- **Visualização de dados:** Usado para análise exploratória (EDA) antes do preprocessamento. Seaborn e Matplotlib
- **Pré processamento de dados:** Transformações necessárias antes de treinar o modelo. StandardScaler e SMOTE
- **Divisão de dados:** Separação entre treino e teste. train_test_split

## Importância no Contexto do Projeto
O pré-processamento é uma etapa essencial do projeto, pois garante que os dados estejam em boas condições para serem analisados e utilizados nos modelos. Caso essa etapa não seja bem feita, os resultados podem sair distorcidos ou pouco confiáveis.

Neste projeto, foi importante tratar problemas comuns como valores ausentes, possíveis inconsistências e dados fora do padrão. Além disso, a padronização e a normalização ajudam alguns modelos a terem um desempenho melhor, já que muitos deles são sensíveis à escala dos dados.

Outro ponto relevante é o balanceamento das classes, principalmente quando há diferença grande entre as categorias. O uso de técnicas como o SMOTE ajuda a evitar que o modelo fique “tendencioso” para a classe majoritária.

A separação entre dados de treino e teste também é fundamental, pois permite avaliar o modelo de forma mais realista, simulando como ele se comportaria com dados novos.

Por fim, os gráficos utilizados ao longo da etapa ajudam a entender melhor os dados, identificar padrões e apoiar as decisões tomadas durante o pré-processamento.

**Link para o arquivo de pré-processamento**: [Pré-processamento](creditcard_pre_processamento.ipynb)
