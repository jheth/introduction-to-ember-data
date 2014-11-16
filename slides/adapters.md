##  Adapters

Know how to talk to the server

* REST (Default)
* ActiveModel (Rails + AMS gem)
* Fixture
* LocalStorage (kurko/ember-localstorage-adapter)

```javascript
window.Blog = Ember.Application.create();

Blog.ApplicationAdapter = DS.LSAdapter.extend({
  namespace: 'blog-emberjs'
});
```

Note:

Can have model specific adapters