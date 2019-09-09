#START NODE STRUCTURE
---
*Based on Rocketseat Template  :)*


**Get Started** 

``` bash
#create files and folders
> sh start
```

**Fix Codes** 

``` bash
#run project
> yarn dev

#fix code on src/
> yarn fix
```


**Folder Structure**

- src
  - app
    - controllers
    - models
  - config
    - database.js
  - database
    - migrations
    - seeds
  - app.js
  - routes.js
  - server.js
- .editorconfig
- .prettierrc
- .sequelizerc
- nodemon.json
---
**Dependencies**

- express
- sequelize
- jsonwebtoken
- bcryptjs
- yup
- dotenv
- pg
- pg-store

**DevDependencies**

- sequelize-cli
- sucrase
- nodemon
- prettier
- eslint
- eslint-config-prettier
- eslint-config-airbnb-base
- eslint-plugin-import
- eslint-plugin-prettier

---

**in .editorconfig**
``` js
root = true
[*]

indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```
**in .prettierrc**
``` json
{
  "singleQuote": true,
  "trailingComma": "es5"
}
```

**in .sequelizerc**
``` js
const { resolve } = require('path');
module.exports = {
  config: resolve(__dirname, 'src', 'config', 'database.js'),
  'models-path': resolve(__dirname, 'src', 'app', 'models'),
  'migrations-path': resolve(__dirname, 'src', 'database', 'migrations'),
  'seeders-path': resolve(__dirname, 'src', 'database', 'seeds'),
};
```
**in nodemon.json**
``` json
{
  "execMap": {
    "js": "sucrase-node"
  }
}
```

**in src/config/database.js**
``` js
require('dotenv/config');
module.exports = {
  dialect: 'process.env.DIALECT',
  host: process.env.DB_HOST,
  username: process.env.DB_USER,
  password: process.env.DB_PASS,
  database: process.env.DB_NAME,
  define: {
    timestamps: true,
    underscored: true,
    underscoredAll: true,
  },
};
```

