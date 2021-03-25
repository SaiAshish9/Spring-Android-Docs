## MongoDB Connection

```
MongoDatabase db=DatabaseConnection.getMongoConnection();
MongoCollection<Document> blocked_users = db.getCollection("<>");
Document filter=new Document();
Iterator<Document> it = blocked_users.find().iterator();
while(it.hasNext()) {
	Document d=it.next();
	System.out.println(d);
}
```
