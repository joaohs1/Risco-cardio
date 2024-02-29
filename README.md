<h1 align="center">O que está mais correlacionado a doenças cardiovasculares?</h1>

<h6 align="left">Para uma visualização completa acesse o notebook - https://github.com/joaohs1/Risco-cardio/blob/main/Doen%C3%A7as%20cardiacas.ipynb)</h6>

<h3 align="left">1. Entendimento do problema</h3>

As doenças cardiovasculares são condições graves que afetam o coração e os vasos sanguíneos, como aterosclerose e hipertensão. Elas são uma das principais causas de morte globalmente. Fatores de risco incluem idade, pressão arterial alta, colesterol elevado, tabagismo e inatividade física. Compreender esses fatores é essencial para prevenir e tratar essas doenças.

Utilizando um dataset do Kaggle (https://www.kaggle.com/datasets/thedevastator/exploring-risk-factors-for-cardiovascular-diseas/data) que contém informações detalhadas sobre os fatores de risco para doenças cardiovasculares. Inclui informações sobre idade, gênero, altura, peso, valores de pressão arterial, níveis de colesterol, níveis de glicose, hábitos de fumar, pratica de atividade, consumo de álcool e se tem problema cardiovascular de mais de 70 mil indivíduos.Com esse dataset vamos focar em um objetivo apenas:

1.	Como manipular os dados e efetuar análises exploratórias para descobrir qual o fator que mais está relacionado a pessoa ter doenças cardiovasculares.

<h3 align="left">2. Importando bibliotecas e Dataset</h3>

Iniciamos importando todas as bibliotecas que serão utilizadas e o dataset:

<img src="/img/import.png" >

<h3 align="left">3. Manipulação/Limpeza dos dados</h3>

Antes de trabalharmos com qualquer dataset, precisamos entender o objetivo principal dos dados, ver se há um dicionário dos dados (o que cada coluna quer dizer) e se os dados do dataframe condiz com o dicionário.
Abaixo segue o dicionário desse dataset:
•	Age: Age of participant (integer)
•	Gender: Gender of participant (male/female).
•	Height: Height measured in centimeters (integer)
•	Weight: Weight measured in kilograms (integer)
•	Ap_hi: Systolic blood pressure reading taken from patient (integer)
•	Ap_lo: Diastolic blood pressure reading taken from patient (integer)
•	Cholesterol: Total cholesterol level read as mg/dl on a scale 0 - 5+ units(integer). Each unit denoting increase/decrease by 20 mg/dL respectively.
•	Gluc: Glucose level read as mmol/l on a scale 0 - 16+ units(integer). Each unit denoting increase Decreaseby 1 mmol/L respectively.
•	Smoke: Whether person smokes or not (binary; 0= No, 1=Yes).
•	Alco: Whether person drinks alcohol or not (binary; 0 =No ,1 =Yes).
•	Active: whether person physically active or not (Binary ;0 =No,1 = Yes).
•	Cardio: whether person suffers from cardiovascular diseases or not (Binary ;0 – no, 1  yes).


<h3 align="left">4. Análise Exploratória dos dados</h3>

Vamos agora analisar cada coluna no intuito de encontrar tendencias importantes ou detectar comportamentos e anomalias.


<p align="center">
<img src="/img/histogramaidade.png" >
</p>


<p align="center">
<img src="/img/distribgene.png" >
</p>


<p align="center">
<img src="/img/distribifuma.png" >
</p>


<p align="center">
<img src="/img/distribbebe.png" >
</p>


<p align="center">
<img src="/img/distribfisica.png" >
</p>


<p align="center">
<img src="/img/distribcard.png" >
</p>


Nessas análises exploratórias univáriavel podemos perceber que nossa população é majoritariamente de homens adultos para idosos com bons hábitos de prática de exercício, não fumam e nem bebem e mesmo assim temos praticamente metade que tende a problemas cardíacos.

Agora vamos cruzar os dados para ver se realmente temos correlação entre eles ou se os problemas cardíacos não têm relação com os dados coletados.


<p align="center">
<img src="/img/fisicacardio.png" >
</p>


<p align="center">
<img src="/img/bebecardio.png" >
</p>


<p align="center">
<img src="/img/fumacardio.png" >
</p>


<p align="center">
<img src="/img/glicocardio.png" >
</p>


<p align="center">
<img src="/img/colestcardio.png" >
</p>


<p align="center">
<img src="/img/idadecardio.png" >
</p>


<p align="center">
<img src="/img/alturacardio.png" >
</p>


<p align="center">
<img src="/img/pesocardio.png" >
</p>


<p align="center">
<img src="/img/imccardio.png" >
</p>

Podemos observar que nessas análises multivariadas o que mais chama atenção de correlação é o IMC e peso que são diretamente proporcionais a doenças cardiovasculares.

Vamos fazer um heatmap para ver correlação geral com todos os dados:


<p align="center">
<img src="/img/cordata.png" >
</p>

E por final, um relatório visual dos dados que mais tem correlação com doença cardiovascular.


<p align="center">
<img src="/img/relatfinal.png" >
</p>


<h3 align="left">5. Conclusão</h3>

Com esses insights gerados pelos cruzamentos de dados, podemos observar que os fatores mais relevantes que estão atrelados no número de pessoas com doenças cardíacas é alto índice de Glicose e colesterol, Peso elevado, IMC elevado e Idade elevada.
Algo que já é uma primícia, mais constatamos mais uma vez com dados é manter bons hábitos para que o IMC seja o ideal, manter os níveis de glicose e colesterol controlados ajuda a não contrair doenças cardíacas.
Os outros fatores apenas por essas análises feitas não foram possíveis correlacionar e nem afirmar se influenciam diretamente se a pessoa tem problemas cardíacos ou não.
Algumas ações para a melhoria dessa análise no futuro é:
•	Desenvolver algoritmo para gerar insights com Pressão arterial, ver o que ela pode influenciar nessas descobertas.
•	Entender o porquê de não ocorrer uma relação mais vertical qual se correlaciona mal hábitos (fumar, não praticar atividade física, beber) com doença cardíaca.
