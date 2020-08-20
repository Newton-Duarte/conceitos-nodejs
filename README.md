<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios-new.png" />

<h3 align="center">Bootcamp GoStack 13 - Desafio: Conceitos do Node.js</h3>

Nesse desafio, devemos criar uma aplicação para armazenar repositórios. A aplicação deve permitir a criação, listagem, atualização e remoção dos repositórios, e além disso permitir que os repositórios possam receber likes.

#### Para esse desafio temos os seguintes testes:

- should be able to create a new repository
- should be able to list the repositories
- should be able to update repository
- should not be able to update a repository that does not exist
- should not be able to update repository likes manually
- should be able to delete the repository
- should not be able to delete a repository that does not exist
- should be able to give a like to the repository
- should not be able to like a repository that does not exist

## Clonar e Testar

`$ git clone https://github.com/Newton-Duarte/conceitos-nodejs`

`$ cd conceitos-nodejs`

`$ yarn` ou `$ npm install`

`$ yarn test` ou `$ npm run test`

![Resultado dos testes](/tests-result.png)

![Resultado dos testes](/gostack-backend.png)

## Rotas da Aplicação

`POST /repositories`
```js
Headers
{
  "Content-Type": "application/json"
}

Body
{
  "title": "Conceitos do Node.js",
  "url": "https://github.com/Newton-Duarte/conceitos-nodejs",
  "techs": ["Node.js", "React.js", "React Native"]
}
```

`GET /repositories`

`PUT /repositories/:id`
```js
Headers
{
  "Content-Type": "application/json"
}

Body
{
  "title": "Conceitos do Node.js",
  "url": "https://github.com/Newton-Duarte/conceitos-nodejs",
  "techs": ["Node.js", "Vue.js"]
}
```

`DELETE /repositories/:id`

`POST /repositories/:id/like`