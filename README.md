
# Mongodb Cheetsheet

This is a mongodb cheetsheeet where almost all the commands of the mongo db are written and you can try this out to learn mongodb fastly and can also refer to this page if you forgot any of it

## Most Commonly Used MongoDB terms

| Common DB Terms | MongoDB Terms |
| :-------- | :------- | 
| Database | Database |
| Tables | Collections |
| Rows | Document |
| Coloums | Fields |

### In MongoDB data are store in BSON




## Some Basic Commands Of Mongodb (Level  -1)

### For invoking Mongo Doemon 
      mongod
### For starting the mongo shell 
      mongo
### To show all the database present in the Mongodb 
      show dbs
### To create a new Database
      use students
### To see the current database 
      db
### To delete the current database which we are in 
      db.dropDatbase()
### To show all the collection in the database 
      show collections
### To create a new collections
      db.createCollection('studentData')
### To delete a collection
      db.studentData.drop()

