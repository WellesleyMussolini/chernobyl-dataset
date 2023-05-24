#  Análise de Dados Exploratória do acidente nuclear de Chernobyl

<div style="display: flex; align-items: center; justify-content: center; width: 100vw;">
  <img src="https://i.ibb.co/s2z4NPy/background-1.png" alt="chernobyl" style="width: 100%" />
</div>

<h1>1. Introdução</h1>
<p>
O acidente nuclear de Chernobyl foi uma explosão ocorrida em 26 de abril de 1986 na usina nuclear de Chernobyl, na Ucrânia. Foi o pior desastre nuclear da história, liberando grandes quantidades de material radioativo na atmosfera, afetando milhares de pessoas e causando impactos ambientais significativos.
</p>

<p>
Este conjunto de dados contém informações sobre casos de câncer em Belarus antes e depois do acidente nuclear de Chernobyl em 1986. Cada linha representa um tipo de câncer, um sexo, um local e um ano e o número de casos de câncer nessa categoria para esse sexo, local e ano. Há informações sobre seis tipos de câncer: pele, tireoide, pulmão, pâncreas, cólon e reto e rim. As informações de local incluem Gomel, Mogilev e Belarus (que é o total para todo o país). Os dados são separados por vírgulas e estão no formato CSV. As informações sobre os anos cobrem 1985 e 1986 e os dados estão desagregados por sexo.
</p>
<br>
<h1>2. Metodologia</h1>

<div style="display: flex; align-items: center; justify-content: center;">
  <table style="text-align: center;">
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
        <td>Cidades afetadas: Mogilev, Belarus, Gomel</td>
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
</div>



<br />

<h2>OBSERVAÇÕES</h2>
<ul>
<li>Os casos são divididos em 2 grupos: casos antes do acidente nos anos de 1977 a 1985 e após o acidente no período de 1986 até 1994.</li>
  <li>Os dados foram coletados para as cidades de Gomel, Mogilev e para todo o país da Bielorrússia.</li>
  <li>Os casos são fornecidos por 100.000 pessoas.</li>
</ul>
<br style="width: 100%" />
<h2>Configuração do Ambiente</h2>
<pre>
 <h3>Linguagem de programação: Python.</h3>
 <h3>Bibliotecas: Pandas.</h3>
</pre>
<br>
<h2>Leitura dos Dados</h2>
<pre>
  <span>CSV</span>
</pre>
<h2>Entre homens e mulheres, qual dos dois sexos tiveram mais casos ?</h2>
<pre>
  <img src="https://i.ibb.co/VYW8dzf/YHYf-Tm-TDNl-AAAAAEl-FTk-Su-Qm-CC.png" alt="cases" />
</pre>
<h2>Apresente os aumentos de casos de câncer entre os anos de 1984 até 1986</h2>
<pre>
  <img src="https://i.ibb.co/QQs6Dxy/casos.png" alt="cases" />
</pre>
<h2>Gráfico com todos os tipos de câncer em mulheres</h2>
<pre>
  <img src="https://i.ibb.co/tDVkSyw/s-Bk-DECBFAjmj-Sp-Imq-V6u8e-PH53-Yp-AJAKZ4-AAAIDp-EIAAAIDpc-Ak-MAACYDme-AAACA6-RCAAACA6-RCAAACA6-RCA.png" alt="cases" />
</pre>
<h2>Gráfico com todos os tipos de câncer em homens</h2>
<pre>
  <img src="https://i.ibb.co/xh4Zm2h/Xf-Xq1d-PYs-WMVGRm-Zp0-Ay-Bkfi-Afgmho3bqzq1atr3-Lhx7i4-FAFxw-RAYAANg-WQQYAANg-Wp5-YAAIBtc-UQGAADYFk.png" alt="cases" />
</pre>
<h2>Regiões afetadas</h2>
<pre>
  <img src="https://i.ibb.co/P184Y08/cities.png" alt="cities" />
</pre>
