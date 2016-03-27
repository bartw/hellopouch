# hellopouch

```shell
npm init
npm install pouchdb --save
npm install http-server -g
npm install http-server --save-dev
```

index.html
```html
<html>

<head>
</head>

<body>
    <script src="node_modules/pouchdb/dist/pouchdb.min.js"></script>
    <script>
        var db = new PouchDB('kittens');
        db.info().then(function (info) {
            console.log(info);
        });
    </script>
</body>

</html>
```

```shell
http-server
```

browse to http://localhost:8080
check dev tools

```js
var doc = {
            "_id": "mittens",
            "name": "Mittens"
        };
        db.put(doc);
        db.get("mittens").then(function (doc) {
           console.log(doc); 
        });
```