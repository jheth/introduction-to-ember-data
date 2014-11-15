##  Features

* Data persistence library
* Models & Relationships
* Adapters (Protocol Abstraction)
* Serializers
* Async/Lazy Loading

Note:

An adapter is an object that knows about your particular server backend and is responsible for translating requests for and changes to records into the appropriate calls to your server.

A serializer is responsible for turning a raw JSON payload returned from your server into a record object.