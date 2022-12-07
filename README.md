# JourneyWithMongodbStarted...

## MongoDB

MongoDB is a type of NoSQL database which is open-sourced and widely used in data science and machine learning in form of a database. Hence, knowledge of it is important in the long run, especially in the field of data science and analytics.

### MongoDB Terminologies
- Document
- Collection
### MongoDB Tools 
- Mongosh
- MongoDB Compass

### MongoDB Database Commands
To view all databases
```bash
show dbs
```
create  or switch to new databases 
```bash
use dbName
```

To view current database
```bash
db
```
To delete database
```bash
db.dropDatabase()
```

### MongoDB commands for collections
To show all the collections
```bash
show collections
```
To create a new collection 
```bash
db.createCollection('collectionName')
```

To delete a collection
```bash
db.collectionName.drop()
ex: db.comment.drop()
```

### MongoDB commands for Rows
To insert Rows
```bash
db.collectionName.insert({
'field':value})

ex:
db.comments.insert({
'name':"Aditya Narayan",
'language':"C"})
```

To show all rows in a collection
```bash
db.comments.find()
```
To show all the rows in a collection in a prettified 
```bash
db.comments.find().pretty()
```


To search rows in MongoDB database
```bash
db.comments.find({'language':"python"})
```
To sort the output rows
```bash
db.collectionName.sort(<objectName>:1 or -1)
Ex:-
sort in asc. order
db.comments.find().sort({language:1})

sort in desc.order
db.comments.find().sort({language:-1})
```
To replace an values in a row
```bash
db.collectionName.replace(filter,replacement,options)
Ex:-
db.comments.replaceOne({language:"C"},{"language":"C++"})
```
Note:-
- If a record that is not available in the collection but we wantto update no operation will perform.
- If a record that is not available in the collection but we want to update if we set upsert is true than it is going to be inserted as new record.
```bash
{upsert:true}
```
