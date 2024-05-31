# Análise de Risco de Crédito no Banco do Futuro

## Criação de um modelo Machine Learning que preveja a probabilidade de inadimplência de um novo cliente, utilizando o KNN Neighbours

## Problema de Negócio
O Banco do Futuro enfrenta desafios significativos na análise de risco de crédito para novos clientes, resultando em inadimplência e perdas financeiras. Para melhorar a precisão e eficiência da análise, a instituição busca desenvolver um modelo de machine learning que automatize o processo de avaliação de crédito.

## Detalhes do Problema
Atualmente, o processo manual de análise de crédito do Banco do Futuro é propenso a erros humanos e inconsistências, resultando em decisões de crédito imprecisas. Estas decisões imprecisas levam a inadimplência, onde os clientes falham em cumprir suas obrigações financeiras, causando perdas financeiras ao banco. A automação deste processo através de um modelo de machine learning pode não apenas acelerar a análise, mas também aumentar a precisão das decisões de crédito, reduzindo o risco de inadimplência.

## Insights da Codificação
A seguir está o processo completo de codificação usado para desenvolver o modelo de machine learning:

## Importação de Bibliotecas
Primeiro, é feito as importações das bibliotecas necessárias:

![Carregamento_Pré_processamento_dos_Dados](img/Carregamento_Pré_processamento_dos_Dados.png)

## Carregamento e Pré-processamento dos Dados
Carregado os dados e realizado a codificação das variáveis categóricas:

----------

Selecionado as colunas relevantes e feito a divisão dos dados entre conjuntos de treinamento e teste:

-----------

Normalizando os dados:

## Treinamento e Avaliação do Modelo
Definindo e treinando o modelo KNN utilizando GridSearchCV para encontrar os melhores hiperparâmetros:

-----------

Previsões no conjunto de teste e avaliação do modelo:


----------------

## Resultados de Avaliação :
## Melhores Hiperparâmetros: 
{'metric': 'manhattan', 'n_neighbors': 5, 'weights': 'distance'}
## Acurácia:
0.8
## Precisão:
0.8702380952380953
## Recall:
0.8
## F1-Score:
0.7859259259259259

## Previsão de Inadimplência
Para prever a probabilidade de inadimplência de um novo cliente:

---------------

## Probabilidades de cada classe:
[0. 0. 0. 0. 1.]

O modelo está extremamente confiante de que o novo cliente pertence à Classe 4, que representa "Negação de crédito".

## Principais Pontos Abordados:
1- Importação e Pré-processamento dos Dados: Codificação das variáveis categóricas e normalização dos dados.

2- Divisão dos Dados: Divisão em conjuntos de treinamento e teste.

3- Modelagem: Uso de KNN com busca de hiperparâmetros utilizando 'GridSearchCV'

4- Avaliação do Modelo: Cálculo de métricas de desempenho como acurácia, precisão, recall e F1-Score.

5- Previsão: Previsão da probabilidade de inadimplência para novos clientes.

## Conclusão e Resumo dos Resultados
O modelo KNN treinado apresentou um bom desempenho com uma acurácia de 0.8 e uma precisão ponderada de aproximadamente 87%. Através da busca de hiperparâmetros, identificamos que o melhor parâmetro para o modelo é 'metric':'n_neighbors': 5. O modelo foi capaz de prever com alta confiança a classe de um novo cliente, indicando sua capacidade de identificar corretamente clientes com risco de crédito. Este modelo pode ser uma ferramenta valiosa para o Banco do Futuro, ajudando a automatizar e melhorar a precisão do processo de análise de crédito.




