writeCode

Write code to:-

- create a database named `sports`.

- list all databases present in local mongod server.
- create 3 collections named `cricket`, `football`, `TT` in sports databse.
- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
- list all collections in sports database.
- rename `TT` collection to `tennis`.
- create a capped collection called `khokho` which should have max 3 documents.
  Try inserting more than 3 and see what happens?
- check whether a collection is capped or not?
- drop all documents from `football` collection.
- delete cricket collection completely.
- delete sports database.
- check which database you are connected to ?
- connect to test database

> use sports
> db.createCollection('cricket')
> db.createCollection('football')
> { "ok" : 1 }
> db.createCollection('TT')
> { "ok" : 1 }
> show dbs
> admin 0.000GB
> config 0.000GB
> local 0.000GB
> sports 0.000GB
> test 0.000GB
> weather 0.000GB
> show collections
> TT
> football
> india
> db.createCollection('cricket')
> { "ok" : 1 }
> show collections
> TT
> cricket
> football
> india
> db.createCollection('Kho Kho' ,{capped:true , size :1024, max :3})
> { "ok" : 1 }
> db.KhoKho.isCapped()
> db.cricket.drop()
> true
> db.dropDatabase()
> { "ok" : 1 }
> db
> test
