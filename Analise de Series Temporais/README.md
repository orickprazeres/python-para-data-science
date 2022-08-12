# Análise de Series Temporais

## Aula 01 - Nessa aula:

* Carregamos um arquivo csv com as vendas da Alucar de 2017 e 2018
* Examinamos o arquivo através de funções do pandas, para descobrir a quantidade de linhas e colunas presentes com o comando `alucar.shape`
* Verificamos se havia dados nulos com o comando `alucar.isna().sum()`
* Alteramos o tipo do `mês` de object para `datetime` com o comando `alucar['mes'] = pd.to_datetime(alucar['mes'])`
* Importamos as bibliotecas necessárias para gerar um gráfico da vendas, porém ao plotar, o gráfico e as labels não estavam num tamanho adequado e sem um título
* Aperfeiçoamos o gráfico incluindo uma nova palette de cor, incluindo título e labels com tamanho adequado descrevendo melhor do que se trata nosso gráfico

## Aula 02 - Nessa aula:

* Aplicamos a técnica de Decomposição de uma time series, para mensurar o crescimento mês a mês
* Utilizamos a função `diff()` para decomposição das vendas para criar o `aumento`, e do aumento para descobrir a `aceleração`
* Executamos a função de `Autocorrelação` para descobrir o nível de correlação das vendas, do aumento e da aceleração
* Criamos uma função chamada `plotar()` e `plot_comparacao()` para geração de gráficos padronizados, evitando código duplicado

## Aula 03 - Nessa aula:

* Vimos a importância da técnica de `Decomposição` na análise dos assinantes da newsletter da Alucar
* Analisamos as vendas da Chocolura e descobrimos um padrão repetitivo no movimento das vendas dentro de um período de tempo fixo, na qual é chamado de `Sazonalidade`
* Examinamos as vendas de uma determinada loja da Chocolura nos meses de Outubro e Novembro de 2018, e descobrimos que também havia uma sazonalidade
* Investigamos o que causava a sazonalidade desta loja

## Aula 04 - Nessa aula:

* Aplicamos a função de `Autocorrelação` nas vendas, no aumento e na aceleração das vendas diárias e vimos que havia uma correlação entre elas
* Executamos uma técnica de `normalização` de time series para minimizar as frequências pela quantidade de dias de finais de semana de cada mês
* Analisamos uma time series importando da biblioteca `statsmodels.tsa.seasonal` a função `seasonal_decompose`, que nos mostra o que é a nossa observação, tendência, sazonalidade e ruído de uma só vez

## Aula 05 - Nessa aula:

* Aprendemos que um componente presente na maioria das Time Series é o `ruído`
* Vimos que podemos minimizar os ruídos de uma time series aplicando a técnica da `média móvel`
* Criamos um gráfico com a média móvel de `7` e `21` dias e comparamos com nossa observação, conforme ilustra a imagem abaixo

