## MongoDB Connection

```
MongoDatabase db=DatabaseConnection.getMongoConnection();
MongoCollection<Document> b = db.getCollection("<>");
Document filter=new Document();
Iterator<Document> it = b.find().iterator();
while(it.hasNext()) {
	Document d=it.next();
	Gson g = new Gson();	
        HashMap m = new HashMap();
        m= g.fromJson(d.getString("<>"),HashMap.class);
        LinkedTreeMap e = (LinkedTreeMap) m.get("<>");
        LinkedTreeMap o = (LinkedTreeMap) m.get("<>");
	System.out.println(d);
}
```
