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







<div data-mime-type="text/markdown" class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput">
<h1 id="2.-Metodologia">2. Metodologia<a href="//github.com/profdiegoaugusto/analise-dados/blob/802bff5b1f5a8c611a208202c1b89740f6710064/Pandas/titanic-eda/#2.-Metodologia" class="anchor-link">¶</a></h1><p>Nesta seção será apresentado todo o processo de preparação, organização e limpeza de dados feito no <em>dataset</em> que possui os seguintes dados:</p>
<table>
<thead>
<tr>
  <th>Coluna</th>
  <th>Descrição</th>
</tr>
</thead>
<tbody>
<tr>
  <td>id_passageiro</td>
  <td>Identficador único do passageiro.</td>
</tr>
<tr>
  <td>classe</td>
  <td>Classe social.</td>
</tr>
<tr>
  <td>sobreviveu</td>
  <td>Sobrevivente? Sim (1), Não (0).</td>
</tr>
<tr>
  <td>nome</td>
  <td>Nome do passageiro.</td>
</tr>
<tr>
  <td>sexo</td>
  <td>Masculino (male), Feminino (female).</td>
</tr>
<tr>
  <td>idade</td>
  <td>Idade do passageiro.</td>
</tr>
<tr>
  <td>irmaos_conjuges</td>
  <td>Número de irmãos e cônjuges a bordo.</td>
</tr>
<tr>
  <td>pais_filhos</td>
  <td>Número de pais e filhos a bordo.</td>
</tr>
<tr>
  <td>bilhete</td>
  <td>Número do bilhete</td>
</tr>
<tr>
  <td>tarifa</td>
  <td>Preço da tarifa do passageiro.</td>
</tr>
<tr>
  <td>cabine</td>
  <td>Cabine.</td>
</tr>
<tr>
  <td>embarque</td>
  <td>Nome do porto de embarque: C = Cherbourg; Q = Queenstown; S = Southampton</td>
</tr>
<tr>
  <td>bote</td>
  <td>Bote salva vidas.</td>
</tr>
<tr>
  <td>corpo</td>
  <td>Número de identificação do corpo.</td>
</tr>
<tr>
  <td>destino</td>
  <td>Local de desembarque do passageiro.</td>
</tr>
</tbody>
</table>
<h2 id="OBSERVA%C3%87%C3%95ES">OBSERVAÇÕES<a href="//github.com/profdiegoaugusto/analise-dados/blob/802bff5b1f5a8c611a208202c1b89740f6710064/Pandas/titanic-eda/#OBSERVA%C3%87%C3%95ES" class="anchor-link">¶</a></h2><ul>
<li><code>classe</code> é uma aproximação do status socioeconômico na época, onde: 1 = Classe Alta1; 2 = Classe Média e 3 = Classe Baixa;</li>
<li><code>idade</code> está representada em anos, porém, se a idade for menor que Um (1) ou caso tenha sido estimada, ela estará com casas decimais xx.5;</li>
<li><code>tarifa</code> está em Libras esterlinas (British Pounds - £) anteriores a 1970;</li>
<li><code>irmaos_conjuges</code> e <code>pais_filhos</code>: as variáveis de relação familiar de algumas relações foram ignoradas; a seguir estão as definições usadas:<ul>
<li><strong>Irmão</strong>: Irmão, irmã, meio-irmão ou meia-irmã do passageiro a bordo do Titanic;</li>
<li><strong>Cônjuge</strong>: Marido ou esposa do passageiro a bordo do Titanic (amantes e noivos ignorados);</li>
<li><strong>Pai</strong>: Mãe ou pai do passageiro a bordo do Titanic;</li>
<li><strong>Criança</strong>: Filho, Filha, Enteado ou Enteada do Passageiro a bordo do Titanic;</li>
<li>Outros parentes excluídos deste estudo incluem primos, sobrinhos / sobrinhas, tias / tios e parentes;</li>
<li>Algumas crianças viajavam apenas com uma babá, portanto foi atribuído 0 para elas em pais_filhos;</li>
<li>Alguns viajaram com amigos ou vizinhos muito próximos em uma vila, no entanto, as definições não apóiam essas relações.</li>
</ul>
</li>
</ul>

</div>






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
