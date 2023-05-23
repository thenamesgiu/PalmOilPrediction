## KDD BR Competition 2018 - Predicting palm oil production

O repositório em questão apresenta uma possível solução para o desafio de previsão de produção de óleo de palama, o dataset se encontra dentro do diretório **dataset**

## O que foi utilizado?

- pandas;
- seaborn;
- sklearn;
- numpy;
- glob;
- matplotlib.

## Processo:

- Verificação de colunas e dados inicialmente pertinentes baseado na inconsistência e similaridade;
- Foram descartados outras colunas Soilwater_L* (exceto Soilwater_L1) pela similaridade quando plotado gráfico em relação à precipitação do momento;
- Dados de anos anteriores a 2006 foram descartados devido à inconsistência de dados desses anos quando plotado o gráfico em relação à produção;
- Aplicação de lag em um período de 12, considerando que há 12 meses no ano (Série temporal);
- Merge dos dataframes de treino e teste com o dataframe de field (após aplicação de lag nos dados) considerando field, month e year - nas rows;
- Alguns valores nulos surgiram em production após o merge, logo, realizei o treinamento do modelo com *HistGradientBoostingRegressor*

**Score: 0.06774241133866515**
