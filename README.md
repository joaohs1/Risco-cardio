<h1 align="center">O que está mais correlacionado a doenças cardiovasculares?</h1>

<h6 align="left">Para uma visualização completa acesse do notebook nos files</h6>

<h3 align="left">1. Entendimento do problema</h3>

As doenças cardiovasculares são condições graves que afetam o coração e os vasos sanguíneos, como aterosclerose e hipertensão. Elas são uma das principais causas de morte globalmente. Fatores de risco incluem idade, pressão arterial alta, colesterol elevado, tabagismo e inatividade física. Compreender esses fatores é essencial para prevenir e tratar essas doenças.

Utilizando um dataset do Kaggle (https://www.kaggle.com/datasets/thedevastator/exploring-risk-factors-for-cardiovascular-diseas/data) que contém informações detalhadas sobre os fatores de risco para doenças cardiovasculares. Inclui informações sobre idade, gênero, altura, peso, valores de pressão arterial, níveis de colesterol, níveis de glicose, hábitos de fumar, pratica de atividade, consumo de álcool e se tem problema cardiovascular de mais de 70 mil indivíduos.Com esse dataset vamos focar em um objetivo apenas:

1.	Como manipular os dados e efetuar análises exploratórias para descobrir qual o fator que mais está relacionado a pessoa ter doenças cardiovasculares.


O Enem (exame nacional do ensino médio) é uma prova aplicada desde 1998 que tem como objetivo avaliar o desempenho de alunos que finalizaram a educação básica. Desde 2009 é composto por quatro matérias e uma redação. Em 2022, cerca de 2,3 milhões de pessoas realizaram as provas, e a missão desse projeto é te mostrar com os dados socioeconômicos, porque há tanta disparidade nas notas das provas respondendo as seguintes perguntas:

  a) Como a renda, escolaridade, idade e região interferem na nota?
  b) Qual dessas características está mais atrelada ao bom desempenho no exame?
 
<h3 align="left">2. Aquisição dos dados</h3>

Todos os dados utilizados nesse projeto são de um dataset com filtro e amostra de 99% de confiança, disponibilizado pelo curso “Ciência de Dados para Finanças e Economia”, retirados do microdados do ENEM de 2019 que está disponível para download no site oficial do ENEM (https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem).

Vamos utilizar 3 bases de dados do dataset indicado acima:

  1.	Dados_Enem
  2.	Dados_Regionais
  3.	Dicionario_Enem

<h3 align="left">3. EDA - análise exploratória de dados</h3>

Aqui vamos fazer algumas plotagens dos dados, para criar insights e tentar responder as perguntas feitas logo no início do projeto, como:

  a) Como a renda, escolaridade, idade e região interferem na nota?
  b) Após realizar a análise acima responder qual dessas características está mais atrelada ao bom desempenho nas provas

Vamos iniciar essa etapa fazendo uma análise geral com a correlação dos dados com HEATMAP.

<p align="center">
<img src="/img/heatmap.png" >
</p>

Se correlacionarmos as notas com renda e tipo da escola, vemos que a nota de matemática tem maior interação com esses itens. Sendo assim para ser mais direto ao ponto podemos utilizar apenas a nota de matemática para nossas análises.

Mas antes disso, vamos procurar a resposta de como a renda interfere em todas as notas, para isso, o BoxPlot pode ser um grande aliado.

Com isso, podemos concluir se realmente podemos utilizar apenas a nota de matemática para nossas análises, e ver mais detalhadamente como é essa correlação entre NOTA x RENDA.

<p align="center">
<img src="/img/boxmat.png">
</p>

<p align="center">
<img src="/img/boxcien.png">
</p>

<p align="center">
<img src="/img/boxcieh.png">
</p>

<p align="center">
<img src="/img/boxling.png">
</p>

Concluímos que independente da matéria abordada, conforme a renda aumenta o desempenho nas notas também cresce. Mas com a nota de matemática podemos ver uma grande diferença nessa correlação. Sendo assim, nas próximas análises utilizaremos apenas a nota de matemática.

Agora vamos levantar um histograma da idade dos participantes:

<p align="center">
<img src="/img/distrib.png">
</p>

Observamos que a maioria dos participantes são jovens de 17 até 19 anos.

Agora vamos fazer análise por regiões, primeiro vamos identificar quantos 
participantes tem por região, e depois iremos ver a média da nota de matemática por região, para entender se existe a relação número de pessoas X Região X Nota de matemática.

<p align="center">
<img src="/img/parreg.png">
</p>

Vamos ver a média de matemática por região.

<p align="center">
<img src="/img/medreg.png">
</p>

Observamos que todas as regiões estão homogêneas, e o número de participantes não está tão correlacionado a ponto de destacar ou diminuir a nota.

Vamos para nossa última análise, entender se o tipo de escola influencia no desempenho (conseguimos fazer uma análise geral, visto que as regiões estão bem homogêneas).

<p align="center">
<img src="/img/privpartreg.png">
</p>
 
No geral, concluímos que o participante de escola particular consegue obter um maior desempenho na prova.

Após todas essas análises, pontualmente fomos chegando a conclusão de nossas perguntas.

Sendo assim, vamos para os últimos passos desse projeto.

<h3 align="left">4. Relatório da análise</h3>

Nesse relatório vamos colocar as visualizações mais importantes e com ele iremos avaliar e concluir esse projeto.

<p align="center">
<img src="/img/relatfin.png">
</p>
 
<h3 align="left">5. Avaliação e conclusão</h3>

Ao longo de todo o projeto, fomos obtendo insights pontuais procurando responder com os dados as duas perguntas feitas no primeiro tópico que são:
  a) Como a renda, escolaridade, idade e região interferem na nota?
  b) Qual dessas características está mais atrelada ao bom desempenho no exame?

Após todos os insights, finalizamos nosso projeto com um relatório final e conseguimos concluir que quando temos dados gerais e sabemos por onde começar, uma das melhores opções é utilizar o HEATMAP (mapa de correlação), pois conseguimos observar que as notas, principalmente de matemática, têm maior correlação com a renda e em seguida, a escolaridade. Logo após, selecionamos uma nota de referência para facilitar a nossa conclusão evitando análises redundantes, com isso utilizamos a análise em BLOXPLOT para selecionar a melhor nota com o critério **maior desvio relacionado a renda**, sendo assim chegamos na **nota de matemática**. Depois, utilizamos essa nota para as demais análises, onde pudemos observar que **idade** (histograma) e **região** (gráfico de barra) não interferem significamente nas notas, pois a idade tem baixa variação e a região está com médias homogêneas, e referente a escolaridade (gráfico de barra) encontramos um desempenho relevante em quem estuda em escola particular. De os itens, a renda é a que mais se correlaciona com o desempenho dos alunos, quanto maior a renda, maior a nota.

