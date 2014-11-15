##  Model

```javascript
var Post = DS.Model.extend({
  title: DS.attr('string'),
  body: DS.attr('string'),
  user: DS.belongsTo('user'),
  comments: DS.hasMany('comment'),
  createdAt: DS.attr('date'),
  isPublished: DS.attr('boolean', {
    default: false
  })
});

```
