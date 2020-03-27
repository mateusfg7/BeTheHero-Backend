
<h1 align="center">

![Be The Hero](doc/logo.svg)

</h1>
<h2 align="center">

[![BACK-END](https://img.shields.io/badge/BACK--END-NodeJS-green?style=flat-square)](https://github.com/mateusfg7/BeTheHero-Backend)
[![FRONT-END](https://img.shields.io/badge/FRONT--END-ReactJS-blue?style=flat-square)](https://github.com/mateusfg7/BeTheHero-Frontend)
[![MOBILE](https://img.shields.io/badge/MOBILE-ReactNative-9cf?style=flat-square)](https://github.com/mateusfg7/BeTheHero-Mobile)

</h2>

<h3 align="center">

_Backend da aplicação 'Be The Hero', feita na Semana OmniStack 11 da Rocketseat_

</h3>

---

## Server
### Iniciar Servidor
```bash
npm start
```
## Database
### Iniciar knex com o arquivo de configuração do banco de dados
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
### Criar Database
```bash
npx knex migrate:latest
```
