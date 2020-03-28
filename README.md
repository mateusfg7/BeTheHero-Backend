
<h1 align="center">

![Be The Hero](doc/logo.svg)

[![BACK-END](https://img.shields.io/badge/BACK--END-NodeJS-green?style=flat-square)](https://github.com/mateusfg7/BeTheHero-Backend)
[![FRONT-END](https://img.shields.io/badge/FRONT--END-ReactJS-blue?style=flat-square)](https://github.com/mateusfg7/BeTheHero-Frontend)
[![MOBILE](https://img.shields.io/badge/MOBILE-ReactNative-9cf?style=flat-square)](https://github.com/mateusfg7/BeTheHero-Mobile)

</h1>

<h3 align="center">

Be The Hero (Seja um herói) é uma aplicação que conecta pessoas que tem vontade de ajudar ONGS doando um valor para tratar algum caso específico.

</h3>
<h4 align="center">

_Back-end da aplicação, feita na **Semana OmniStack 11** da **Rocketseat**_

_(23/03/20 a 27/03/20)_

[TO-DO + Anotações](https://github.com/users/mateusfg7/projects/4)

© [Rocketseat](https://rocketseat.com.br/)

Instrutor: [Diego Fernandes](https://github.com/diego3g)
</h4>

---

**App feito com [Node JS]()**

## Instalar dependências
```bash
npm install
```
## Iniciar knex com o arquivo de configuração do banco de dados
```bash
npx knex init
```
### Arquivo de configuração **knexfile.js**
```JS
// Update with your config settings.

module.exports = {

  development: {
    client: 'sqlite3',
    connection: {
      filename: './src/database/db.sqlite'
    },
    migrations: {
      directory: './src/database/migrations'
    },
    useNullAsDefault: true,
  },
  
  test: {
    client: 'sqlite3',
    connection: {
      filename: './src/database/test.sqlite'
    },
    migrations: {
      directory: './src/database/migrations'
    },
    useNullAsDefault: true,
  },

  staging: {
    client: 'postgresql',
    connection: {
      database: 'my_db',
      user:     'username',
      password: 'password'
    },
    pool: {
      min: 2,
      max: 10
    },
    migrations: {
      tableName: 'knex_migrations'
    }
  },

  production: {
    client: 'postgresql',
    connection: {
      database: 'my_db',
      user:     'username',
      password: 'password'
    },
    pool: {
      min: 2,
      max: 10
    },
    migrations: {
      tableName: 'knex_migrations'
    }
  }

};
```
## Criar Database
```bash
npx knex migrate:latest
```
## Iniciar Servidor
```bash
npm start
```
## Estrutura

- `tests/` -> pasta com tetes automatisados
- `tests/unit` -> pasta com tetes unitários
- `tests/Integration` -> pasta com tetes de rotas
- `src/app.js` -> arquivo principal
- `src/routes.js` -> arquivo de rotas 
- `src/server.js` -> arquivo para ativar servidor
- `src/utils` -> funções úteis 
- `src/database` -> arquivos de configuração e conexão com o banco de dados