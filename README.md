
# Mongodb Cheetsheet

This is a mongodb cheetsheeet where almost all the commands of the mongo db are written and you can try this out to learn mongodb fastly and can also refer to this page if you forgot any of it

## Most Commonly Used MongoDB terms

| Common DB Terms | MongoDB Terms |
| :-------- | :------- | 
| Database | Database |
| Tables | Collections |
| Rows | Document |
| Coloums | Fields |

### In MongoDB data are store in BSON not in JSON format




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
### To insert a document in the collections
    db.studentData.insert({name : "Jack", age : 20})
### For inserting only one document into the collections (same work as " .insert() ")
    db.studentData.insertOne({
        name : "Travour", 
        email : "travor458@gmail.com",
        age : 24
        })
### For inserting multiple document into the collections
    db.studentData.insertMany([
        {name : "Harry", email : "marry234@gmail.com", age : 13}, 
        {name : "Ronit", email : "ronit@outlook.com", age : 45}, 
        {name : "Adesh", email : "sadhuadesh@gmail.com", age : 18}
        ])
### For displaying the documents present inside the collections
    db.studentData.find()
### For displaying the documents present inside the collections in a prettyer format
    db.studentData.find().pretty()
### For displaying the limited number of document present in the collection
    db.studentData.find().limit(3).pretty()
### For counting the number of document present in the collections
    db.studentData.find().count()
### For sorting the document in ascending order on the basis of age
    db.studentData.find().sort({age : 1})
### For sorting the document in descending order on the basis of age
    db.studentData.find().sort({age : -1})
### For chaining multiple function together
    db.studentData.find().limit(2).sort({age : -1}).pretty()
### For finding only one document 
    db.studentData.findOne({age : 18})
## Atomic / Update Operator
| Atomic Operator | Use Of This Operator |
| :-------- | :------- | 
| $set | Updating the stored document without changing the prev. state of the document |
| $inc | To increment and decrement on the numerical type variable |
| $push | Push new field but it must be of ARRAY type field |
| $eq     |    Matches values that are equal to the given value. |
|$gt     |    Matches if values are greater than the given value.|
|$lt     |    Matches if values are less than the given value.|
|$gte    |    Matches if values are greater or equal to the given value.|
|$lte    |    Matches if values are less or equal to the given value.|
|$in     |    Matches any of the values in an array.|
|$ne     |    Matches values that are not equal to the given value.|
|$nin    |    Matches none of the values specified in an array.|

### For finding a group of documents based on some condition
    db.studentData.findOne({age : {$lte : 18}})


# More Comming Soon...
