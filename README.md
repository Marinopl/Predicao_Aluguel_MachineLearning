# Predição de Aluguéis de Imóveis na cidade de São Paulo

---

## Objetivo

* Entender como o valor do aluguel na cidade de São Paulo varia conforme diferentes features são incluídas, como Bairro, valor de taxas e Metragem, a partir de uma base de dados [disponível no Kaggle da Imobilíaria Quinto Andar](https://www.kaggle.com/datasets/dantebarros/transformed-data-from-quinto-andars-platform).
  - A predição gerada pelo algoritmo de Machine Learning é um insight de negócio: saber em quais imóveis investir que trarão um rápido retorno financeiro a partir da valorização do preço do aluguel.
 
* Um dos objetivos deste projeto é entender como é a metodologia CRISPM, desde a Limpeza dos Dados, Análise Exploratória, Feature Enginniering and Selection e, por fim, a Produção do modelo.

## Etapas

1. [Entendimento e Data Cleaning](#dados)
2. [Análise Exploratória (EDA)](#eda)
3. [Tratamento dos Dados](#tratamento)
4. [Definição do modelo](#modelo)
5. [Modelo em produção](#producao)

---

<a id='dados'></a>
## Entendimento e Data Cleaning

* Esta é a primeira etapa do projeto e uma das mais importantes. Limpar uma base de dados utilizando o Pandas pode parecer simples, mas é crucial, pois utilizar uma base de dados com valores inconsistentes (outliers) ou valores nulos e faltantes, gera ruído no modelo, resultando em péssimas predições.
  - Aqui, utilizou-se a biblioteca Pandas para realizar o entendimento dos dados que vieram de uma base .csv, com valores nulos e faltantes;
  - Utilizou-se o site da Imobiliária Quinto Andar para entender os valores inconsistentes e faltantes;
 
---

<a id='eda'></a>
## Análise Exploratória de Dados

* A análise exploratória consiste em entender, principalmente, a estatística que a base de dados pode apresentar, como Média, Moda, Mediana, Quartis, Desvio Padrão e Outliers
  - Realizar esta etapa é crucial para tratarmos os dados de maneira que a essência da base não seja perdida, tornando-a consistente para entrar no modelo de Machine Learning;
  - Estudou-se as correlações e dispersões entre as features da base de dados.

---

<a id='tratamento'></a>
## Tratamento dos dados

* Nesta etapa foi realizado o processo de Feature Selection e Feature Enginniering, para definir quais variáveis entrarão no modelo.

---

<a id='modelo'></a>
## Definição do modelo

* Definir o algoritmo de Machine Learning é uma etapa importante. Como queremos uma previsão dos valores de aluguel, vamos utilizar modelos de Machine Learning de Regressão.
  - Aqui foram testados três tipos: Árvore de Decisão por Regressão, Regressão Linear e RandomForest por Regressão
  - O modelo escolhido foi baseado na métrica *Mean Absolute Error*, tentando entender o quanto o modelo estava errando. O modelo escolhido foi *RandomForest por Regressão*
