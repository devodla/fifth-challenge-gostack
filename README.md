<h1 align="center">
    <img alt="GoStack" src="https://rocketseat-cdn.s3-sa-east-1.amazonaws.com/bootcamp-header.png" width="200px" />
</h1>

<h3 align="center">
  Challenge 5: First project with ReactJS
</h3>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/onlyreynaldo/fifth-challenge-gostack?color=%2304D361">

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <img alt="Last commit" src="https://img.shields.io/github/last-commit/onlyreynaldo/fifth-challenge-gostack?style=flat-square" >

  <a href="https://github.com/onlyreynaldo/fifth-challenge-gostack/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/onlyreynaldo/fifth-challenge-gostack?style=social">
  </a>
</p>

## :rocket: Features

### 1. Catching errors

A `try/catch` has been added around the code present in the `handleSubmit` function in the `Main` component if a repository is not found in the Github API around the input where the user entered the repository name will have a red border.

### 2. Duplicated repository

Before calling the API in the `handleSubmit` function, you have a check to see if the repository is not duplicated, that is, if it does not already exist in the `repositories` state.

If it does exist, it sends an error, and with that the code will fall into the `catch` of the `try/catch` created in the previous functionality.

```js
throw new Error('Duplicated repository');
```

### 3. Status filter

A status filter has been added to the Issues listing in the repository detail. The status represents whether the issue is open, closed or an option to display all.

Examples of requests:

```
https://api.github.com/repos/rocketseat/unform/issues?state=all
https://api.github.com/repos/rocketseat/unform/issues?state=open
https://api.github.com/repos/rocketseat/unform/issues?state=closed
```

### 4. Pagination

Paging has been added to the issues listed in the repository detail. The Github API lists a maximum of 30 issues per page.

```
https://api.github.com/repos/rocketseat/unform/issues?page=2
```