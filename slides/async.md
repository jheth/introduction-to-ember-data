##  Async

```javascript
  comments: DS.hasMany('comment', {async: true})
```

Embedded IDs, but no data.

```javascript
{
  "post": {
    "title": "Ember Data",
    "body": "How it works...",
    "comment_ids": [1,2,3]
  }
}
```

Lazy Load Comments

```javascript
post.get('comments') => GET "/comments?ids[]=1,ids[]=2,ids[]=3"
```