# DB Module of powered by json files 

## Installation
```
npm install drahovdb
```

## Functions

- **add(dataname,value)**


- **get(dataname)**


- **has(dataname)**


- **remove(dataname)**


- **copy(filename)**


- **increase(dataname,value)**


- **reduce(dataname,value)**


- **clear()**


## Descriptions
- **add:** Writes any value to dataname.


- **get:** Gets value by dataname from filename.


- **has:** Returnes true if the dataname has.


- **remove:** Deletes any data from file.


- **copy:** Copies the file to any file.


- **increase:** If the value is number and the data is value you can increase the data.


- **reduce:** If the value is number and the data is value you can reduce the data.


- **clear:** Deletes all datas from file.


# Examples<br/>
### Constructor
```js
const { Database } = require('drahovdb')

const db = new Database('file') //write file name without .json!
```
### Add
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.add('nick','drahov') //adds database.json "nick":"drahov" data
```
### Get
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.get('nick') //returns drahov
```

### Has
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.has('nick') //returns true
```

### Remove
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.remove('nick') //deletes nick data
```

### Copy
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.copy('database_copy') //copies database.json to database_copy.json
```

### Increase
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.add('int',10)

db.increase('int',1) //increases int value 1
```

### Reduce
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.reduce('int',1) //reduces int value 1
```

### Copy
```js
const { Database } = require('drahovdb')

const db = new Database('database')

db.clear() //deletes all datas from database.json
```

```js
const db = require('drahovdb')

db.write('nick','drahov','nickdata') //returns true when the process is complete
db.get('nick','nickdata') //returns drahov 
db.has('name','nickdata') //returns false because nickdata doesnt have data of named name
db.delete('nick','nickdata') //deletes nick data from nickdata.json file
db.backup('nickdata','nickdata_copy') //copies nickdata file to nickdata_copy
db.plus('int','1','data') //1 increases int data in data.json
db.minus('int','1','data') //1 reduces int data in data.json
db.deleteall('data') //deletes all datas in data file
```


# Notice


**Please write filenames without .json**

[github](www.github.com/Drahov/Db-Module)<br/>
