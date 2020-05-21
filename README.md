<h1 align="center">Banco de dados e upload de arquivos no Node.js</h1>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/amandavianna/desafio-database-upload">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/amandavianna/desafio-database-upload?color=%2304D361">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/amandavianna/desafio-database-upload">

  <a href="https://github.com/amandavianna/desafio-database-upload/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/amandavianna/desafio-database-upload.svg">
  </a>
</p>

<p>É uma aplicação para armazenar transações financeiras de entrada e saída, que permite o cadastro e a listagem dessas transações, além de permitir a criação de novos registros no banco de dados a partir do envio de um arquivo csv.</p>

## Rotas da aplicação:

- **`POST /transactions`**: A rota recebe title, value, type e category dentro do corpo da requisição, sendo type o tipo da transação, que deve ser income para entradas (depósitos) e outcome para saidas (retiradas);

- **`GET /transactions`**: Rota que lista todas as transações que você cadastrou até agora, junto com o valor de soma de entradas, retiradas e total de crédito.

- **`DELETE /transactions/:id`**: Deleta uma transação com o id presente nos parâmetros da rota;

- **`POST /transactions/import`**: A rota permite a importação de um arquivo com formato .csv contendo as mesmas informações necessárias para criação de uma transação, onde cada linha do arquivo CSV deve ser um novo registro para o banco de dados. Modelo do arquivo [.csv](https://github.com/amandavianna/desafio-database-upload/blob/master/src/__tests__/import_template.csv).


## Como usar:

```bash
# Clone this repository
$ git clone https://github.com/amandavianna/desafio-database-upload

# Go into the repository
$ cd desafio-database-upload

# Install dependencies
$ yarn

# Run the app
$ yarn dev:server
```
