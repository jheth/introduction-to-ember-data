##  Find

```javascript
// Array
this.store.find('post')
GET "/posts" => [ {post: {id: 1, ...} }, {post: {id: 2, ...} } ]

// Find Multiple
this.store.find('post', {ids: [1,2,3]});
GET "/posts?ids[]=1&ids[]=2&ids[]=3" => [{},{},{}]

// Query String parameters
this.store.find('post', {hasComments: true, sort_by: 'created_at'})
GET "/posts?hasComments=true&sort_by=created_at" => [{post: ...}]
```

```javascript
// Single Record
this.store.find('post', 1)
GET "/posts/1" => {post: {id: 1, ...} }
```

```javascript
// Return local records
var posts = this.store.all('post'); // => no network request
```
