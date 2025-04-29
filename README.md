# Cadastro de Produtos com Streamlit e Azure

Este projeto é uma aplicação de cadastro de produtos construída com **Streamlit**, utilizando **Azure Blob Storage** para armazenar imagens e **Microsoft SQL Server** para gerenciar os dados.

## Funcionalidades

- Cadastro de produtos com:
  - Nome do produto
  - Preço do produto
  - Descrição do produto
  - Imagem do produto
- Listagem de produtos cadastrados com exibição em formato de cards.
- Armazenamento de imagens no **Azure Blob Storage**.
- Persistência dos dados em um banco de dados SQL Server.

## Tecnologias Utilizadas

- [Streamlit](https://streamlit.io/): Framework Python para criação de aplicações web interativas.
- [Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/): Serviço de armazenamento de arquivos na nuvem.
- [pymssql](http://www.pymssql.org/): Biblioteca para conectar-se ao Microsoft SQL Server.
- [dotenv](https://pypi.org/project/python-dotenv/): Utilizada para carregar variáveis de ambiente de forma segura.

## Estrutura do Código

O código principal contém:

1. Formulário para cadastro de produtos.
2. Função `upload_blob` para armazenar imagens no Azure Blob Storage.
3. Função `insert_product` para inserir os dados do produto no banco SQL Server.
4. Função `list_products` para recuperar produtos cadastrados.
5. Exibição de produtos cadastrados em formato de cards utilizando Streamlit.

## Configuração

### Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto e defina as seguintes variáveis:

```plaintext
BLOB_CONNECTION_STRING=<sua_connection_string>
BLOB_CONTAINER_NAME=<nome_do_container>
BLOB_ACCOUNT_NAME=<nome_da_conta>

SQL_SERVER=<endereco_do_servidor>
SQL_DATABASE=<nome_do_banco_de_dados>
SQL_USER=<usuario_sql>
SQL_PASSWORD=<senha_sql>
