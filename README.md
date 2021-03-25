## MongoDB Connection

```
MongoDatabase db=DatabaseConnection.getMongoConnection();
MongoCollection<Document> b = db.getCollection("<>");
Document filter=new Document();
Iterator<Document> it = b.find().iterator();
while(it.hasNext()) {
	Document d=it.next();
	System.out.println(d);
}
```
