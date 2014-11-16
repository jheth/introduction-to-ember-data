##  Delete

```javascript
this.store.find('post', 1).then(function (post) {
  post.deleteRecord();
  post.get('isDeleted'); // => true
  post.save(); // => DELETE /posts/1
});

// OR
this.store.find('post', 2).then(function (post) {
  post.destroyRecord(); // => DELETE /posts/2
});
```
