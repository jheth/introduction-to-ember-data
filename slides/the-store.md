##  The Store

* Client Cache (in-browser)
* Model Lifecycle (new, dirty, deleted)
* Available to all controllers and routes
* Central repository of records (Single Source of Truth)
* Operations return a Promise

Note:

The store is the central repository of records in your application. You can think of the store as a cache of all of the records available in your app. Both your application's controllers and routes have access to this shared store; when they need to display or modify a record, they will first ask the store for it.

This instance of DS.Store is created for you automatically and is shared among all of the objects in your application.