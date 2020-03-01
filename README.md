<h1 align="center">
    <img alt="GoStack" src="https://rocketseat-cdn.s3-sa-east-1.amazonaws.com/bootcamp-header.png" width="200px" />
</h1>

<h3 align="center">
  Desafio 5: Primeiro projeto com ReactJS
</h3>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/onlyreynaldo/fifth-challenge-gostack?color=%2304D361">

  <img alt="License" src="https://img.shields.io/github/license/onlyreynaldo/fifth-challenge-gostack?style=flat-square">

  <img alt="Last commit" src="https://img.shields.io/github/last-commit/onlyreynaldo/fifth-challenge-gostack?style=flat-square" >

  <a href="https://github.com/onlyreynaldo/fifth-challenge-gostack/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/onlyreynaldo/fifth-challenge-gostack?style=social">
  </a>
</p>

## :rocket: Funcionalidades

### 1. Captando erros

Foi adicionado um `try/catch` por volta do código presente na função `handleSubmit` presente no componente `Main` se caso um repositório não seja encontrado na API do Github por volta do input em que o usuário digitou o nome do repositório terá uma borda vermelha.

### 2. Repositório duplicado

Antes de fazer a chamada à API na função `handleSubmit` tem uma verificação para ver se o repositório não está duplicado, ou seja, se ele ainda não existe no estado de `repositories`.

Caso exista, manda um erro, e com isso o código cairá no `catch` do `try/catch` criado na funcionalidade anterior.

```js
throw new Error('Repositório duplicado');
```

### 3. Filtro de estado

Foi adicionado um filtro de estado na listagem de Issues, no detalhe do repositório. O estado representa se a issue está em aberto, fechada ou uma opção para exibir todas.

Exemplos de requisição:

```
https://api.github.com/repos/rocketseat/unform/issues?state=all
https://api.github.com/repos/rocketseat/unform/issues?state=open
https://api.github.com/repos/rocketseat/unform/issues?state=closed
```

### 4. Paginação

Foi adicionado paginação nas issues listadas no detalhe do repositório. A API do Github lista no máximo 30 issues por página.

```
https://api.github.com/repos/rocketseat/unform/issues?page=2
```