<h1 style="text-align: center;">Be The Hero</h1>
<h2 style="text-align: center;">

![[Back-End]('https://github.com/mateusfg7/BeTheHero-Backend')]('https://img.shields.io/badge/Back--End-NodeJS-green?style=flat-square')
![[Front-End]('https://github.com/mateusfg7/BeTheHero-Frontend')]('https://img.shields.io/badge/Front--End-ReactJS-blue?style=flat-square')
![[Mobile]('https://github.com/mateusfg7/BeTheHero-Mobile')]('https://img.shields.io/badge/Mobile-ReactNative-9cf?style=flat-square')

</h2>

_Backend da aplicação 'Be The Hero', feita na Semana OmniStack 11 da Rocketseat_

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
