<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>README</title>
  </head>
  <body>
    <h1>README</h1>

    <p>Este código contém um programa de ETL (Extração, Transformação e Carga) que realiza a leitura de arquivos da B3, filtra os dados e os concatena em um único arquivo CSV. O programa está escrito em Python e utiliza as bibliotecas Pandas e Datetime.</p>

    <h2>Funcionamento do programa</h2>

    <p>O programa é composto pelas seguintes funções:</p>

    <ul>
      <li><code>read_files</code>: realiza a leitura de um arquivo da B3, utilizando o método <code>read_fwf</code> da biblioteca Pandas. A função recebe quatro parâmetros: <code>path</code>, que é o caminho onde o arquivo está armazenado; <code>name_file</code>, que é o nome do arquivo; <code>year_date</code>, que é o ano que está sendo lido; e <code>type_file</code>, que é o tipo do arquivo (txt, por exemplo). A função retorna um dataframe com os dados do arquivo lido.</li>
      <li><code>filter_stocks</code>: filtra os dados do dataframe para manter apenas as ações de código BDI 2, que são as ações padrão da B3. A função recebe um dataframe como parâmetro e retorna o mesmo dataframe com as ações filtradas.</li>
      <li><code>parse_date</code>: converte a coluna de datas do dataframe para o formato datetime. A função recebe um dataframe como parâmetro e retorna o mesmo dataframe com a coluna de datas convertida.</li>
      <li><code>parse_values</code>: converte as colunas de preços do dataframe para o formato float, dividindo o valor por 100. A função recebe um dataframe como parâmetro e retorna o mesmo dataframe com as colunas de preços convertidas.</li>
      <li><code>concat_files</code>: realiza a leitura de vários arquivos da B3, utilizando a função <code>read_files</code>, e concatena os dados em um único dataframe. A função recebe cinco parâmetros: <code>path</code>, que é o caminho onde os arquivos estão armazenados; <code>name_file</code>, que é o nome base dos arquivos; <code>year_date</code>, que é uma lista com os anos que devem ser lidos; <code>type_file</code>, que é o tipo dos arquivos (txt, por exemplo); e <code>final_file</code>, que é o nome do arquivo CSV que será gerado com os dados concatenados. A função não retorna nada, mas gera um arquivo CSV com os dados concatenados.</li>
    </ul>

    <p>Para executar o programa, basta chamar a função <code>concat_files</code>, passando os parâmetros desejados.</p>

    <h2>Exemplo de uso</h2>

    <p>Aqui está um exemplo de como utilizar o programa:</p>

    <pre><code>year_date = ['2018', '2019', '2020']
path = ''
name_file = 'COTAHIST_A'
type_file = 'txt
