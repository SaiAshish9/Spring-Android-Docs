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

## Config

```
DbConnection.java
String str="mongodb://saiashish:saiashish@localhost:27017/mydb?retryWrites=true";
builder.hosts(Arrays.asList(new ServerAddress("127.0.0.1", 27017))))
```

## Git Config

```
To set your global username/email configuration:
Open the command line.

Set your username:
git config --global user.name "FIRST_NAME LAST_NAME"

Set your email address:
git config --global user.email "MY_NAME@example.com"

To set repository-specific username/email configuration:
From the command line, change into the repository directory.

Set your username:
git config user.name "FIRST_NAME LAST_NAME"

Set your email address:
git config user.email "MY_NAME@example.com"

Verify your configuration by displaying your configuration file:
cat .git/config
```
