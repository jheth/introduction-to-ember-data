##  Unloading

Removes from local store, no network request

```javascript
// Remove single record
this.store.find('post', 1).then(function(post) {
  post.unloadRecord();
  // OR
  this.store.unloadRecord(post);
});

// Remove all from local store.
this.store.unloadAll( 'post' );
```
