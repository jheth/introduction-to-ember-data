##  Create

```javascript
var post = this.store.createRecord('post', {
  title: 'Ember Data',
  body: 'Lorem ipsum'
});

// Set relationship after object is loaded.
this.store.find('user', 1).then(function(user) {
  post.set('author', user);
});
```

Note:

The store object is available in controllers and routes using this.store.