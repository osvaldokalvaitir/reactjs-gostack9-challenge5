# ReactJS - Desafio 5 (Novo)

[![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/osvaldokalvaitir/reactjs-desafio5-novo/blob/master/LICENSE)
![](https://img.shields.io/github/package-json/v/osvaldokalvaitir/reactjs-desafio5-novo.svg)
![](https://img.shields.io/github/last-commit/osvaldokalvaitir/reactjs-desafio5-novo.svg?color=red)
![](https://img.shields.io/github/languages/top/osvaldokalvaitir/reactjs-desafio5-novo.svg?color=yellow)
![](https://img.shields.io/github/languages/count/osvaldokalvaitir/reactjs-desafio5-novo.svg?color=lightgrey)
![](https://img.shields.io/github/languages/code-size/osvaldokalvaitir/reactjs-desafio5-novo.svg)
![](https://img.shields.io/github/repo-size/osvaldokalvaitir/reactjs-desafio5-novo.svg?color=blueviolet)
[![made-for-VSCode](https://img.shields.io/badge/Made%20for-VSCode-1f425f.svg)](https://code.visualstudio.com/)
![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)

Aplicação usando Create React App, ESLint, Prettier, EditorConfig, React Router, styled-components, React Icons, Axios e prop-types.

## Desafio 05. Aplicação com ReactJS

Nesse desafio você adicionará novas funcionalidades na aplicação que desenvolvemos ao longo desse módulo.

### Funcionalidades

#### Captando erros

Adicione um `try/catch` por volta do código presente na função `handleSubmit` presente no componente `Main` e caso um repositório não seja encontrado na API do Github adicione uma borda vermelha por volta do input em que o usuário digitou o nome do repositório.

#### Repositório duplicado

Antes de fazer a chamada à API na função `handleSubmit` faça uma verificação para ver se o repositório não está duplicado, ou seja, se ele ainda não existe no estado de `repositories`.

Caso exista, dispare um erro, e com isso o código cairá no `catch` do `try/catch` criado na funcionalidade anterior.

```js
throw new Error('Repositório duplicado');
```

#### Filtro de estado

Adicione um filtro de estado na listagem de Issues que criamos no detalhe do repositório. O estado representa se a issue está em aberto, fechada ou uma opção para exibir todas.

Exemplos de requisição:

```
https://api.github.com/repos/rocketseat/unform/issues?state=all
https://api.github.com/repos/rocketseat/unform/issues?state=open
https://api.github.com/repos/rocketseat/unform/issues?state=closed
```

Você pode encontrar a documentação [nesse link](https://developer.github.com/v3/issues/#parameters-1);

#### Paginação

Adicione paginação nas issues listadas no detalhe do repositório. A API do Github lista no máximo 30 issues por página e você pode controlar o número da página atual por um parâmetro no endereço da requisição:

```
https://api.github.com/repos/rocketseat/unform/issues?page=2
```

Adicione apenas um botão de próxima página e página anteior. O botão de página anterior deve ficar desativado na primeira página.

## Índice

- [Capturas de Tela](#capturas-de-tela)

  - [Principal](#principal)

  - [Repositório](#repositório)

- [Desenvolvimento](#desenvolvimento)

  - [Configuração do Ambiente](#configuração-do-ambiente)

  - [Instalação do Projeto](#instalação-do-projeto)

  - [Execução do Projeto](#execução-do-projeto)

- [Utilizados no Projeto](#utilizados-no-projeto)

  - [Bibliotecas](#bibliotecas)

  - [APIs](#apis)

## Capturas de Tela

### Principal

![Main](/.github/assets/main.png)
Esta é a primeira tela, onde encontram-se todos os repositórios do GitHub que o usuário pesquisar na caixa de texto.

### Repositório

![Repository](/.github/assets/repository.png)
Nesta tela, encontram-se todas as issues referentes ao repositório selecionado pelo usuário, podendo escolher somente as issues abertas ou fechadas, é possível também abrir a página da issue ou voltar para a página inicial.

## Desenvolvimento

### Configuração do Ambiente

Clique [aqui](https://github.com/osvaldokalvaitir/projects-settings/blob/master/README.md) e siga `Configuração de Ambiente`.

### Instalação do Projeto

Clique [aqui](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/nodejs.md) e siga `Instalação de Projeto`.

### Execução do Projeto

Clique [aqui](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/create-react-app.md) e siga `Execução de Projeto para Desenvolvimento` ou `Construção e Execução de Projeto para Produção`.

## Utilizados no Projeto

### Bibliotecas

- [Axios](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/axios.md)

- [babel-eslint](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/babel-eslint.md)

- [Create React App](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/create-react-app.md)

- [ESLint](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/eslint.md)

- [eslint-config-prettier](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/eslint-config-prettier.md)

- [eslint-plugin-prettier](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/eslint-plugin-prettier.md)

- [Prettier](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/prettier.md)

- [prop-types](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/prop-types.md)

- [React Icons](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/react-icons.md)

- [react-router-dom](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/react-router-dom.md)

- [styled-components](https://github.com/osvaldokalvaitir/projects-settings/blob/master/nodejs/libs/styled-components.md)

### APIs

- **[GitHub](https://api.github.com)**

  - **Rotas**

    - Usuários

      - Busca dados de um repositório pertencente a um usuário
      - Busca issues de um repositório pertencente a um usuário
