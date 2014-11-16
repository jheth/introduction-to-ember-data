##  Model Lifecycle

* isNew
* isValid
* isLoaded
* isDirty
* isSaving (in-flight)
* isDeleted
* isError

Note:

isLoaded - The adapter has finished retrieving the current state of the record from its backend.
isDirty - The record has local changes that have not yet been saved by the adapter. This includes records that have been created (but not yet saved) or deleted.
isSaving - The record has been sent to the adapter to have its changes saved to the backend, but the adapter has not yet confirmed that the changes were successful.
isDeleted - The record was marked for deletion. When isDeleted is true and isDirty is true, the record is deleted locally but the deletion was not yet persisted. When isSaving is true, the change is in-flight. When both isDirty and isSaving are false, the change has been saved.
isError - The adapter reported that it was unable to save local changes to the backend. This may also result in the record having its isValid property become false if the adapter reported that server-side validations failed.
isNew - The record was created locally and the adapter did not yet report that it was successfully saved.
isValid - No client-side validations have failed and the adapter did not report any server-side validation failures.