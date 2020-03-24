# BeTheHero-Backend
Backend da aplicação 'Be The Hero', feita na Semana Omnistack 11 da Rocketseat

---

## Iniciar Servidor
```bash
npm start
```

## Iniciar knex com o arquivo de configuração do banco de dados

```bash
npx knex init
```

Arquivo de configuração **knexfile.js**

```JS
// Update with your config settings.

module.exports = {

  development: {
    client: 'sqlite3',
    connection: {
      filename: './src/database/db.sqlite'
    }
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