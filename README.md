**# Projeto Dados do Censo UCI

O repositório contém arquivos do projeto de machine learning que utiliza a base de dados do censo.

- O objetivo do projeto é prever se renda anual de um indivíduo é superior a $50.000 por ano com base em dados do censo.

- **Dataset**: O conjunto de dados para este projeto é originário do [Repositório de Aprendizado de Máquina da UCI](https://archive.ics.uci.edu/ml/datasets/Adult)

- O histórico dos resultados das previsões é mostrado abaixo, bem como um resumo das técnicas e ferramentas que foram utilizadas para desenvolver o projeto:

-

---
## [Parte 1: Primeiro modelo](LINK PARTE 1)
- Na primeira parte do projeto foi realizada uma **análise preliminar** da **base de dados** com **tratamentos simples** para avaliar o desempenho do **modelo** em um conjunto básico, estabelecendo uma **linha de base** para comparações e otimizações futuras.
- Os datasets com os dados brutos não estavam formatados corretamente, então foi necessário realizar a manipulação, limpeza e tratamentos dos arquivos csv.
- Com as bases de treino e teste tratadas corretamente para que sejam importadas como um dataframe, gerou-se um **relatório** usando a biblioteca **ydata_profiling**, que fornece uma **análise exploratória** rápida e resumida, facilitando a compreensão das **características dos dados** e apoiando **decisões** para etapas posteriores.
- A coluna target 'income' foi transformada de categórica para numérica utilizando o .map({'>50K': 1, '<=50K': 0})
- Os dados duplicados e todos as colunas categóricas restantes foram removidas.
- Foram criados três **modelos** utilizando os algoritmos '**RandomForest**', '**KNN**' e '**LogisticRegression**'.  
- Os modelos foram avaliados utilizando a **acurácia**, **precisão**, a **matriz de confusão** e o **relatório de classificação**.
- A previsão do modelo final obteve as seguintes pontuações (utilizando o modelo **RandomForest**):
  - Acurácia: **0.**.
  - Precisão: ****.

## [Parte 2: Análise e Tratamentos mais Avançados](https://github.com/douglashideki/Titanic/blob/main/Titanic%20-%20Parte%202/Titanic%20-%20Parte%202.ipynb)
- Na **segunda parte** do projeto, foi realizada uma **análise exploratória** mais detalhada em cada coluna do **conjunto de dados**.  
- Inicialmente foi retirado o **título** pertencente a cada passageiro e então codificado com o **get_dummies**.  
