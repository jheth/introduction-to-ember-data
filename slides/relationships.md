##  Relationships

#### Side Loading

```javascript
{
  "post": {"title": 'My Post', "comment_ids": [1,2,3], "user_id": 1},
  "comments": [
    {'id': 1, ...}, {'id': 2, ...}
  ],
  "users": [
    {'id': 1, ...}
  ]
}
```

#### Embedded Mixin

```javascript
App.PostSerializer = DS.RESTSerializer.extend(DS.EmbeddedRecordsMixin, {
  attrs: {
    comments: { embedded: 'always' }
  }
});
```

Note:

Explicit inverses