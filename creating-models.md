---
description: How to define Models in Sequelize
---

# Creating Models

#### Defining a Model

```javascript
const Sequelize = require("sequelize");
const sequelize = new Sequelize('database', 'user', 'password', {
	host: 'localhost',
	dialect: 'sqlite', // using sqlite3 here (must install sqlite3 to use it)
	logging: false,
	storage: 'database.sqlite'
});

const database = sequelize.define('nameOfTheTable', {
	key: Sequelize.STRING, // more datatypes can be found at Sequelize Docs
	value: Sequelize.NUMBER
});
```

#### Syncing the Models

* The `Async/Await` Method

```javascript
await database.sync();
console.log('Database Loaded!')
```

* The `.then` method

```javascript
database
    .sync()
    .then(() => console.log('Database Loaded!'));
```

