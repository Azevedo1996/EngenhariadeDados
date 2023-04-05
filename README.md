Este é um script em Python que realiza a extração, transformação e carga (ETL) de dados da Bovespa. Ele lê um conjunto de arquivos de texto com informações diárias de negociação da bolsa, filtra apenas as ações do tipo 2 e salva todas as informações em um arquivo CSV único.

Bibliotecas
O script utiliza apenas uma biblioteca do Python:

Pandas (importada como pd) - utilizada para a leitura dos arquivos de texto, manipulação dos dados e escrita no arquivo CSV.
Funções
O script contém quatro funções:

read_files: lê um arquivo de texto com informações diárias de negociação da bolsa, utiliza o formato "fixed width" e retorna um DataFrame com as informações lidas.

filter_stocks: filtra apenas as ações do tipo 2 e remove a coluna codbdi.

parse_date: converte a coluna data_pregao de string para formato de data.

parse_values: converte as colunas preco_abertura, preco_maximo, preco_minimo e preco_fechamento de string para formato float.

concat_files: executa as funções read_files, filter_stocks, parse_date e parse_values em uma lista de arquivos de texto, concatena os DataFrames resultantes e salva todas as informações em um arquivo CSV único.

Uso
Para utilizar o script, é necessário informar o caminho para os arquivos de texto, o nome base do arquivo, a lista de anos que se deseja processar e o nome do arquivo CSV final. É possível também ajustar a posição das colunas e o nome das colunas do arquivo original editando as variáveis colspecs e names na função read_files.

