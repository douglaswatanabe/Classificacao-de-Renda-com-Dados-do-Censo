# Projeto Dados do Censo UCI

O repositório contém arquivos do projeto de machine learning que utiliza a base de dados do censo.

- **Objetivo:** O objetivo do projeto é prever se renda anual de um indivíduo é superior a $50.000 por ano com base em dados do censo.

- **Dataset:** O conjunto de dados para este projeto é originário do [Repositório de Aprendizado de Máquina da UCI](https://archive.ics.uci.edu/ml/datasets/Adult)

- O histórico dos resultados das previsões é mostrado abaixo:

<img src = 'https://github.com/douglashideki/UCI-Census-Income-Dataset/blob/main/img/resultados.png'>

---
## [Parte 1: Primeiro modelo](LINK PARTE 1)
- Na primeira parte do projeto foi realizada uma **análise preliminar** da base de dados com **tratamentos simples** para avaliar o desempenho do modelo em um conjunto básico, estabelecendo uma **linha de base** para **comparações** e **otimizações futuras**.  

- **Limpeza dos Dados Brutos:**
  - Os **datasets brutos** foram **manipulados** e **tratados** para corrigir **formatações inadequadas** nos arquivos CSV.  

- **Importação e Relatório de Análise:**
  - Após a limpeza dos dados brutos, os dados foram **importados como `dataframes`**. Um **relatório exploratório** foi gerado usando a biblioteca **`ydata_profiling`** para facilitar a **análise preliminar** das **características dos dados**.
   
- **Tratamentos:**
  - A **coluna target** `'income'` foi convertida de **categórica para numérica** utilizando o **`.map({'>50K': 1, '<=50K': 0})`**.
  - Os **dados duplicados** e as demais **colunas categóricas** foram **removidas**. 

- **Modelagem:**
  - Foram criados **três modelos** utilizando os algoritmos: **`RandomForest`**, **`KNN`** e **`LogisticRegression`**.  

- **Avaliação:**
  - Os **modelos** foram avaliados por **métricas** como **acurácia, precisão, matriz de confusão e relatório de classificação**.  

- **Resultados:**
  - O **modelo final (RandomForest)** apresentou os seguintes **resultados** para a previsão da base de teste:  
    - **Acurácia: 0.8087**.  
    - **Precisão: 0.6154**.  
 

## [Parte 2: Análise e Tratamentos mais Avançados](LINK PARTE 2)
- Na **segunda parte** do projeto, foi realizada uma **análise exploratória** mais detalhada em cada **coluna** do **conjunto de dados**.  

- **Tratamentos:**
  - Diferente da **primeira parte**, onde as **colunas categóricas** foram removidas, nesta parte todas elas foram **analisadas**, **tratadas** e **convertidas para numéricas**. Também foram feitas **classificações** em algumas **colunas numéricas**, **criação de novas colunas** e a **remoção de outras**.  
    - Foi utilizado o **`get_dummies`** e o **`OneHotEncoder`** para codificar as **colunas categóricas** onde os valores não possuem **ordem de importância**, pois estas técnicas criam uma **coluna para cada categoria** com o valor **0 ou 1**.  
    - Já para as **colunas categóricas** que possuem um certo tipo de **ordenação**, foi utilizado o **`OrdinalEncoder`**.  
  - Além disso, foram utilizadas técnicas como a **criação de funções**, **list comprehension**, **`.apply()` e `lambda`**, e **`.qcut()`** para dividir os **dados em grupos** de tamanhos aproximadamente iguais.  
  - Foram utilizadas as bibliotecas **seaborn** e **matplotlib** para plotar diversos **gráficos**, como o **gráfico de barras**, de **distribuição** e de **linhas**.  
  - Para as análises, foram utilizadas técnicas como **`.groupby()`**, **`.corr()`**, **`.crosstab()`**, **`.concat()`**, e outras.  

- **Modelagem e Avaliação:**
  - Foram utilizados os mesmos **modelos** e **métricas de avaliação** da **parte 1**.  

- **Resultados:**
  - O **modelo final** (**RandomForest**) apresentou os seguintes **resultados** para a **previsão** da **base de teste**:  
    - **Acurácia:** **0.8562**.  
    - **Precisão:** **0.7503**.
 

## [Parte 3: Modelo Final](LINK PARTE 3)
- **Tratamentos:**  
  - Com os **dados em escala diferentes**, foi realizada a **padronização dos dados** utilizando o **`StandardScaler`**, que faz a **reescala** dos **dados** para que tenham **média zero** e **desvio padrão igual a 1**.  
  - Também foi feita a **seleção de features** para escolher as **variáveis** ou **atributos mais relevantes** para o **modelo** e descartar aquelas que são **irrelevantes**, **redundantes** ou **ruidosas**.  

- **Modelagem:**  
  - Além dos modelos **`RandomForest`** e **`KNN`** utilizados anteriormente, nesta parte do projeto também foram utilizados os modelos **`DecisionTree`** e **`MLPClassifier`**.  

- **Avaliação:**  
  - Além das métricas utilizadas anteriormente, foi utilizado o **F1 Score** e a **validação cruzada**.  
    - A métrica **F1** foi utilizada pois pode ser interpretada como uma **média harmônica** da **precisão** e **recall**, combinando dessa forma as duas métricas de maneira **equilibrada**.  
    - Foi utilizada a técnica de **validação cruzada** com a finalidade de **avaliar** o **desempenho dos modelos** de maneira **mais precisa e robusta**.  

- **Otimização de Hiperparâmetros:**  
  - Por fim, foi realizado o **`GridSearchCV`** para **ajustar os hiperparâmetros** dos **modelos**, realizando uma **busca sistemática** para encontrar a **combinação ideal de parâmetros** que **maximize o desempenho** do **modelo** e **previna overfitting**.  

- **Resultados:**  
  - O **modelo final** (**RandomForest**) apresentou os seguintes **resultados** para a **previsão** da **base de teste**:  
    - **Acurácia:** **0.8636**.  
    - **Precisão:** **0.7681**.  
