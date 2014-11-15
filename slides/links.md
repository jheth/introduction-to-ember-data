##  Async with Links

```javascript
  comments: DS.hasMany('comment', {async: true})
  user: DS.belongsTo('user', {async: true})
```

```javascript
// Links
{
  "post": {
    "title": "Ember Data",
    "body": "How it works...",
    "links": {
      "comments": "/post/1/comments",
      "user": "/user/9"
    }
  }
```

Lazy Load Comments

```javascript
post.get('comments') => GET "/post/1/comments"
post.get('user') => GET "/user/9"
```
