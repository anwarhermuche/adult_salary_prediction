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

<img src="https://i.ibb.co/n8v7XRt/Screenshot-3.png">

A dimensão do dataset é 32561 linhas e 15 colunas. 

Sobre os valores faltantes, nós não temos nesse dataset. Além disso, os tipos de dados variam entre string e inteiros.

Abaixo, você pode encontrar uma análise estatística breve do dataset:

<img src="https://i.ibb.co/ygvNZGJ/Screenshot-1.png">

## 🗺️ Descriptive Analysis

Aqui, vou responder as 4 perguntas que me propus a responder.

1. Há um salto muito grande no salário de bacharéis, mestres e doutores?

<img src="https://i.ibb.co/30WKWkf/Screenshot-2.png">
<img src="https://i.ibb.co/6Nb3W68/Screenshot-4.png">

2. O valor da hora trabalhada aumenta com o aumento da escolaridade? 

<img src="https://i.ibb.co/jLCJr5s/Screenshot-5.png">

Infelizmente, não é possível extrair tantos insights, visto que há apenas dois grupos salariais e não o valor exato. Isso nos impede de fazer qualquer afirmação com relação ao valor salario/hora. 

Entretanto, é importante notar que para todos os níveis educacionais, com exceção do nível pré-escolar, o número médio de horas trabalhadas por semana, para o mesmo nível educacional, aumentou do grupo que ganha menos ou igual a 50k por ano para o grupo que ganha mais de 50k. Mais precisamente, o aumento foi de 17.93% 

Além disso, não há pessoas com o nível pré-escolar que recebem mais de 50k por ano.

3. Solteiros ganham mais que pessoas em algum tipo de relacionamento?

<img src="https://i.ibb.co/vzsJJxX/Screenshot-7.png">

Como podemos ver, claramente solteiros não ganham mais que pessoas em relacionamento. Na verdade, maridos e esposas são os dois status de relacionamento que possuem maior porcentagem de pessoas que ganham mais de 50k por ano.

4. Com o aumento do nível de escolaridade, a proporção de homens e mulheres se mantém? E a proporção de brancos e negros?

<img src="https://i.ibb.co/hcw6GMk/Screenshot-8.png">

Agora, vamos utilizar os mesmos códigos para responder a segunda pergunta.

<img src="https://i.ibb.co/7XnL0p6/Screenshot-9.png">

Com isso, vamos responder as duas perguntas:

Os dois níveis de escolaridade mais altos ("Doctorate" e "Prof-school") são aqueles onde há a menor porcentagem de mulheres. Além disso, a proporção média de mulheres é 30.18%, atingindo um mínimo de 16% no nível "Prof-school". Portanto, fica evidente que a proporção não se mantém quando o nível de escolaridade aumenta. 

Agora, falando sobre a proporção de brancos e negros, temos que os 4 níveis de escolaridade mais altos são aqueles em que há menos negros e 7 dos 9 níveis de escolaridade mais baixos são aqueles em que há mais negros. Além disso, a proporção média de negros é de 10.11%, atingindo um mínimo de 2.84% no nível "Prof-school". Sendo assim, novamente, fica claro que a proporção de negros diminui consideravelmente à medida em que o nível de escolaridade aumenta.

## 📈 The Prediction & Conclusion

Para fazer a predição, testei vários modelos com a validação cruzada e o modelo que apresentou a melhor performance foi o Gradient Boosting Classifier, da biblioteca ensemble, do scikit-learn.

Os resultados dos modelos foram estes:

<img src="https://i.ibb.co/JFf6RF3/Screenshot-10.png">

Verificação no conjunto de testes:

<img src="https://i.ibb.co/nmxQxZf/Screenshot-11.png">

## ✅ Conclusão

Como vimos, nosso melhor modelo alcançou 86.91% de acurácia, 70.29% de F1-Score e 79.19% de ROC AUC.

Para um modelo sem ensemble, tunagem de parâmetros e qualquer outro tipo de otimização, é um bom resultado para o primeiro ciclo do CRISP-DM.
