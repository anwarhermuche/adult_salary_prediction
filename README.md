# Predição de salários - Gradient Boosting Classifier

****

## 🔍 Sobre o projeto

Neste projeto, vamos fazer uma análise dos dados coletados a partir do censo de 1994 dos EUA.

Além disso, o objetivo é construir um modelo de Machine Learning que consiga prever, a partir das características de cada indivíduo, se essa pessoa faz mais de $ 50K por ano.

Você pode baixar o dataset <a href="https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data" target="_blank">clicando aqui</a>.

## 🗃️ Tópicos do projeto

O projeto é dividido nos seguintes tópicos:
<ol>
  <li> Importando bibliotecas
  <li> Análise estrutural do dataset
  <li> Análises Univariadas e Multivariadas
  <li> Pré-processamento dos dados
  <li> Validação cruzada
  <li> Verificação do desempenho no conjunto de teste
  <li> Conclusão
</ol>

## 📍 Descrição do dataset

Primeiramente, vamos ver as primeiras 5 linhas do dataset

<img src="data:image/png;base64,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">

A dimensão do dataset é 32561 linhas e 15 colunas. 

Sobre os valores faltantes, nós não temos nesse dataset. Além disso, os tipos de dados variam entre string e inteiros.

Abaixo, você pode encontrar uma análise estatística breve do dataset:

<img src="https://i.ibb.co/MkmZWGq/Screenshot-8.png">

We can see that Adj Close column is equal to Close column, so we can exclude it to make the dataset more clean.

## 🗺️ Descriptive Analysis

Let's start visualizing the graph that shows the close price variation during the period

<img src="https://i.ibb.co/YpN2bRp/Screenshot-1.png">

We can clearly see that the most important part of this analysis is between 2021 and 2022, so let's take a look more closer. 

Starting with 2021:

<img src="https://i.ibb.co/bNHf68T/Screenshot-2.png">

In this period, we've reached the maximum close price of dogecoin at 05/07/2021. 

Now, 2022:

<img src="https://i.ibb.co/852fmCZ/Screenshot-3.png">

We can see that the price started falling down again.

I know that when we talk about stock market we try to profit it. So, nothing better than looking at moments that gave to the investitors the biggest profits. I'm gonna look just at 2021, which was the year of price boom. 

And to start this analysis, let's take a look at the daily and monthly close price variation:

<img src="https://i.ibb.co/wBGfb4Q/Screenshot-4.png">

In 2021, we had 884 days with positive close price variation; 844 days with negative close price variation; and 8 days with no close price variation. 

In addition, the maximum postive price variation was 0.1433. And the minimum negative price variation was -0.1843 in a day.

Now, let's see the montly close price variation

<img src="https://i.ibb.co/fkFBKbX/Screenshot-5.png">

We had 6 months with positive price variation and 6 months with negative price variation.

Ok, we've just seen the variations between dates in the same year, but we know that some people invest their money and keep it there for years to get a great profit. So we need to look at the whole dataset, and this is what I did. 

I created a loop to tell me all the profits greater than 100% between all the dates since 2017. Take a look:

<img src="https://i.ibb.co/zs316cW/Screenshot-9.png">

Analysing this dataframe, we can extract the following insights of 2021:

<ul>
  <li> The average number of days to have a profit between 100% and 200% was 172 
  <li> The average profit was 12.22x
  <li> The max profit was 157.57x, and it happened buying at 2021/01/01 and selling at 2021/05/08, i.e. 127.0 days between the buy and sell
</ul>

## 📈 The Prediction & Conclusion

To predict the dogecoin's close price, I used autots package. According to it's official documentation, AutoTS is a time series package for Python designed for rapidly deploying high-accuracy forecasts at scale. 

There are dozens of forecasting models usable in the sklearn. These includes naive, statistical, machine learning, and deep learning models.

After predicting, these are the values that the algorithm returned:

<img src="https://i.ibb.co/GQVBCwt/Screenshot-6.png">

Plotting in a graphic:

<img src="https://i.ibb.co/cJCGzWZ/Screenshot-7.png">

Analysing this, we can see that the close price probabily is gonna raise at the next days.

That's it! Be aware of the prices to make good decisions at stock market. Thank you for your attention!
