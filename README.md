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
        m= g.fromJson(d.getString("json"),HashMap.class);
        LinkedTreeMap event_host = (LinkedTreeMap) m.get("event_host");
        LinkedTreeMap owner = (LinkedTreeMap) m.get("owner");
	System.out.println(d);
}
```
