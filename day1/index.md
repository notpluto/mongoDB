- create a database named `sports`.
use sports

- list all databases present in local mongod server.
show dbs

- create 3 collections named `cricket`, `football`, `TT` in sports databse.

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `cost`.
db.cricket.insert({name: "Sachin", age: "23", email: "abc@gmail.com", cost: "20k"}, {name:"jumbo", age: "21", email: "sam@gmail.com", cost: "12k"})

db.football.insert({name: "Messi", age: "31", email: "messi@gmail.com", cost: "20L"}, {name:"Suarez", age: "31", email: "rez@gmail.com", cost: "31K"})

db.TT.insert({name: "Mukesh", age: "27", email: "messi@gmail.com", cost: "20L"}, {name:"Ramesh", age: "23", email: "rez@gmail.com", cost: "31K"})

- list all collections in sports database.
db.getCollectionNames()

- rename `TT` collection to `tennis`.
db.TT.renameCollection('Tennis')

- create a capped collection called `khokho` which should have max 3 documents.
db.createCollection("khokho", {capped: true, size: 2, max: 3})

-Try inserting more than 3 and see what happens?
Older documents are removed

- check whether a collection is capped or not?
db.khokho.isCapped()

- drop all documents from `football` collection.
db.football.remove({})

- delete cricket collection completely.
db.cricket.drop()

- delete sports database. 
db.dropDatabase()

