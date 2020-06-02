# COVID-19BR-cli_tracker

Bash script que atualiza, formata e imprime no terminal os dados relativos à distribuição de casos de COVID-19 por município brasileiro de acordo com a base de dados disponibilizada em [Brasil.io](https://brasil.io).

## Sobre o Brasil.io 

O Brasil.io é uma iniciativa que visa apresentar em formato acessível os dados tornados públicos em virtude da [Lei de Acesso à Informação](http://www.planalto.gov.br/ccivil_03/_Ato2011-2014/2011/Lei/L12527.htm). Leia [o manifesto do Brasil.io](https://brasil.io/manifesto/), para mais informações.      

## Sobre o ESPECIAL COVID-19 

*O ESPECIAL COVID-19 - Dados por Município* é uma iniciativa promovida pelo Brasil.io que diariamente compila os boletins epidemiológicos publicados pelas Secretarias Estaduais de Saúde, apresentando os dados em uma série histórica contendo a distribuição de casos confirmados de COVID-19 por município brasileiro, o número de óbitos, novos casos, dentre outras informações relevantes. Acesse a [página](https://brasil.io/covid19/), para mais informações.      

## Sobre o script 

O script possibilita que a usuária acesse os dados sobre a COVID-19 no Brasil [disponibilizados no site do Brasil.io](https://brasil.io/dataset/covid19/caso_full/) a partir do terminal, permitindo que ela acompanhe a evolução dos casos da doença nos municípios brasileiros sem que para isso seja preciso acessar o navegador.

Ao utilizar o script, a usuária poderá:

* Atualizar a base de dados 
* Filtrar os dados por estado, município, data de atualização, etc.  
* Visualizar os dados de acordo com as seguintes categorias: 

	* DATA: data de atualização
	* DIAS: número de dias desde que o primeiro caso de COVID-19 foi confirmado no município       
	* UF: unidade federativa à qual o município pertence
	* MUNICÍPIO: nome do município 
	* No_DE_CASOS: número total de casos de COVID-19 confirmados no município  
	* NOVOS_CASOS: número de novos casos confirmados no município desde a última atualização
	* No_DE_ÓBITOS: número total de óbitos por COVID-19 confirmados no município   
	* NOVOS_ÓBITOS: número de novos óbitos confirmados no município desde a última atualização
	* MORTALIDADE: taxa de mortalidade por COVID-19 no município    
	* POPULAÇÃO: estimativa do número de habitantes no município em 2019   

## Dependências

* wget 

## Instruções de uso

Basta digitar o seguinte comando no terminal para obter a tabela completa dos dados relativos à COVID-19 no Brasil: 

>>$./covidbr

(assumindo-se que a usuária encontra-se no mesmo diretório em que o script foi salvo)        

Na primeira vez em que o script é executado, ele realiza o download automático do [arquivo CSV](https://brasil.io/dataset/covid19/caso_full/?format=csv) disponível na página do Brasil.io. Após o arquivo ser salvo na pasta de Downloads da usuária, o seu conteúdo é formatado e impresso no terminal. Em todas as outras vezes em que o script é executado, a usuária terá acesso à data e horário da última atualização, podendo ou não optar por atualizar a base de dados novamente.

Há duas formas de filtrar os dados a serem apresentados. A primeira delas envolve digitar o filtro imediatamente após o script:

>>$./covidbr São Paulo

>>$./covidbr são paulo

>>$./covidbr SP

>>$./covidbr sp

A segunda forma consiste em executar o script sem argumentos e só então digitar o filtro. 

## Screenshots

![image_01](/images/image_01.png)

![image_02](/images/image_02.png)

![image_03](/images/image_03.png)

![image_04](/images/image_04.png)
