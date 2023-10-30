## V1
```js
const mongoose = require("mongoose");  
async function connect(){  
    let result;  
    try {  
        result = await mongoose.connect('mongodb://127.0.0.1:27017/mflix');  
    } catch (error) {  
        result = error;  
    }  
    return result;  
}  
connect().then(result => {  
    console.log(result);  
    console.log(`closing connection ...`);  
    mongoose.connection.close();  
}).catch(err => {  
    console.error(err);  
})
```
## V2
```js
const mongoose = require('mongoose');  
let dbConfig = require('./db.config');  
async function main() {  
    let conString = `${dbConfig.HOST}/${dbConfig.DB}`;  
    console.log(`connect to ${conString}`);  
    await mongoose.connect(`${conString}`);  
}  
  
main()  
    .then(data => {  
        console.log(data)  
        mongoose.connection.close();  
    })  
    .catch(err => console.log(err));
```