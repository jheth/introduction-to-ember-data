##  Update

```javascript
var user = this.store.find('user', 9);

// ...after the record has loaded
user.incrementProperty('postCount');
user.set('isAdmin', true);

person.get('isDirty');    // => true
user.changedAttributes(); // => { isAdmin: [false, true], postCount: [2, 3] }

user.save();              // => POST /users/9
// OR
user.rollback();          // => reverts local state
user.get('isDirty');      // => false

// OR
user.reload();            // => GET /users/9
```

Note:
Promise is always returned
