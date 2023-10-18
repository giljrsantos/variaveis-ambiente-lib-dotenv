# Utilizando variáveis de ambiente em aplicações Node.js com a lib dotenv

Ao criar uma aplicação, é comum ter valores que podem variar ao longo do código dependendo do ambiente em que a aplicação está sendo executada. Por exemplo, a string de conexão com o banco de dados pode ser diferente dependendo do ambiente onde o código está sendo executado, porém o código fonte em si é exatamente o mesmo independente do ambiente. Nesse contexto torna-se vantajoso parametrizar estes valores por meio do uso de variáveis de ambiente.

Para ler o valor de uma variável de ambiente, podemos utilizar a propriedade env do módulo process.

## Explicação

Quando executamos a aplicação, a linha require("dotenv").config() é executada. Esta linha lê o arquivo .env e carrega seus valores no process.env. Que então pode ser acessado ao longo da aplicação.

## Vantagens

A ideia geral é que seja possível parametrizar valores que sua aplicação necessita que variam de acordo com o ambiente. Por exemplo, o nível de log no localhost pode ser muito mais detalhado que no ambiente de produção, onde normalmente registramos somente as mensagens de erro.


