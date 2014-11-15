##  Pushing

```javascript
this.store.push('post', {
  id: 1,
  title: "Ember.js",
  body: "A javascript framework."
});

// Patch
var updateEvent = {id: 1, title: "New Title"};
this.store.update('post', updateEvent);
```

```javascript
var pushData = {
  posts: [
    {id: 1, post_title: "Great post", comment_ids: [2]}
  ],
  comments: [
    {id: 2, comment_body: "Insightful comment"}
  ]
}

this.store.pushPayload(pushData);
```

Note:
All objects in Ember must have an 'id' attribute.