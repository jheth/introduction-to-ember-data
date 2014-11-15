##  Metadata

Ember Data's JSON deserializer looks for a meta key:

```javascript
var result = this.store.find("post", { limit: 10, offset: 0 });
```

```javascript
{
  "posts": [
    { "id": 1, "title": "My First Blog Post" },
    { "id": 2, "title": "My Second Blog Post" }
  ],
  "meta": {
    "total": 100,
    "page": 0
  }
}
```

```javascript
var meta = this.store.metadataFor("post");
// meta.total => 100

// Or you can access the metadata just for this query:

var meta = result.get("content.meta");
```