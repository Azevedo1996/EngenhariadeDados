Processamento de dados de arquivos históricos da B3
Este repositório contém um conjunto de funções em Python para realizar o processamento de arquivos históricos de negociações de ações na B3 (Bolsa de Valores, Mercadorias e Futuros de São Paulo). Esses arquivos contêm dados de preços de ações e outras informações relevantes que podem ser úteis para análises financeiras.

As funções são projetadas para extrair informações relevantes dos arquivos e transformá-las em um formato de tabela, que pode ser facilmente manipulado e analisado em outros programas ou bibliotecas Python. O código foi desenvolvido usando a biblioteca pandas, uma biblioteca poderosa e eficiente para a análise de dados em Python.

Funcionalidades
O código deste repositório possui as seguintes funcionalidades principais:

Ler arquivos de texto com formato posicional de dados históricos da B3.
Extrair informações relevantes dos arquivos, como preços de abertura, fechamento, máximo e mínimo, além de volume de negociações e outras informações relevantes.
Converter os dados extraídos em um formato de tabela pandas para fácil manipulação.
Filtrar as ações de interesse, usando o código BDI da B3 para identificar ações comuns.
Tratar os campos de data e valores numéricos para que possam ser usados em cálculos ou gráficos.
Como usar
O código é composto por várias funções, que podem ser utilizadas em conjunto para realizar o processamento completo dos dados. O fluxo principal do código é o seguinte:

Ler os arquivos de dados com a função read_files.
Filtrar as ações de interesse com a função filter_stocks.
Converter o campo de data com a função parse_date.
Converter os valores numéricos com a função parse_values.
Concatenar todos os arquivos em um único arquivo CSV com a função concat_files.
O uso dessas funções pode ser facilmente adaptado para diferentes conjuntos de dados de arquivos históricos da B3. Basta fornecer o caminho para os arquivos, o nome do arquivo e as datas de interesse.

Exemplo de uso
Para usar este código em seus próprios projetos, siga os seguintes passos:

Baixe o repositório em seu computador.

Instale as dependências necessárias listadas em requirements.txt. Isso pode ser feito usando o comando pip install -r requirements.txt.

Adicione seus próprios arquivos de dados históricos da B3 à pasta de dados do repositório. Certifique-se de que seus arquivos estejam no formato posicional de arquivo de texto.

Abra o arquivo main.py e atualize os parâmetros do caminho do arquivo, o nome do arquivo e as datas de interesse para se adequar aos seus próprios arquivos.

Execute o arquivo main.py para iniciar o processamento de dados.
