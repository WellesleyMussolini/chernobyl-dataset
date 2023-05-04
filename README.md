# dataset

# 1. Introdução
O acidente nuclear de Chernobyl foi uma explosão ocorrida em 26 de abril de 1986 na usina nuclear de Chernobyl, na Ucrânia. Foi o pior desastre nuclear da história, liberando grandes quantidades de material radioativo na atmosfera, afetando milhares de pessoas e causando impactos ambientais significativos.

O conjunto de dados deste estudo contém informações sobre o número de casos de câncer em Belarus antes e depois do acidente em Chernobyl. Esses dados foram publicados em um artigo científico da revista "Radiation and Risk" e foram coletados e fornecidos pelo Centro de Tecnologias Médicas de Belarus. O conjunto de dados divide os casos em dois grupos: casos antes do acidente, de 1977 a 1985, e casos após o acidente, de 1986 a 1994. No conjunto de dados, foram usadas duas datas para facilitar a operação: 1985 e 1986, referindo-se aos períodos de 1977 a 1985 e de 1986 a 1994, respectivamente. Os dados foram coletados para as cidades de Gomel e Mogilev, além de todo o país de Belarus. As informações são apresentadas em termos de casos por 100.000 habitantes.

<h1>2. Metodologia</h1>

<p>
<table>
<thead>
<tr>
  <th>Coluna</th>
  <th>Descrição</th>
</tr>
</thead>
<tbody>
<tr>
  <td>year</td>
  <td>ano do ocorrido</td>
</tr>
<tr>
  <td>sex</td>
  <td>Diferenciação se é homem ou mulher</td>
</tr>
<tr>
  <td>location</td>
  <td>Cidades de Belarus</td>
</tr>
<tr>
  <td>cancer_type</td>
  <td>Tipo de câncer que foi adquirido</td>
</tr>
<tr>
  <td>cases</td>
  <td>quantidade de casos registrados</td>
</tr>
</tbody>
</table>
</p>

<h2>2.1. Configuração do Ambiente</h2>
<pre>
<span>Visual Studio Code: editor e leitor de código.</span>
<span>Python: linguagem de programação.</span>
</pre>

<h2>2.2. Leitura dos Dados</h2>
<pre>
<span>Pandas: O pandas é uma biblioteca em Python que foi utilizada para a análise e manipulação de dados no projeto. Com essa ferramenta, foi possível carregar o conjunto de dados em um formato de tabela, o que facilita a visualização e manipulação dos dados.</span>
<span>CSV: A leitura dos dados utilizados do dataset neste trabalho estão no formato CSV (Comma Separated Values), que é um formato de arquivo comum para armazenar e trocar dados tabulares. A leitura dos dados foi realizada utilizando a biblioteca Pandas do Python, que possui uma função específica para carregar dados em formato CSV</span>
</pre>

<h2>2.3. Organização e Limpeza dos Dados</h2>
<h3>2.3.1. Visão Geral do Conjunto de Dados</h3>
<pre><span></span></pre>
<pre><span></span></pre>

<h3>2.3.2 Remoção de Colunas</h3>
Remoção de colunas incompletas e/ou desnecessárias para a análise.
<pre><span></span></pre>

<h3>2.3.3. Dados Ausentes</h3>
<pre><span></span></pre>

<h3>2.3.3.1 Idades Ausentes</h3>
Para os dados ausentes da coluna idade será feita a substituição dos dados vazios pela média das idades na época.
<pre><span></span></pre>

<h3>2.3.3.2 Tarifas Ausentes</h3>
<p>Para os dados ausentes da coluna <code>tarifa</code>será feita a substituição dos dados vazios pela média de preço das tarifas na época.</p>

<h3>2.3.3.3 Portos de Embarque Ausentes</h3>
<p>Para os dados ausentes da coluna <code>embarque</code>será feita a remoção dos dados vazios.</p>
<pre><span></span></pre>
