# Class 32

## DRF Permissions

Permissions determine whether a request should be granted or denied access.

Permission checks are always run at the very start of the view, before any other code is allowed to proceed.

Permission checks will typically use the authentication information in the request.user
 and request.auth properties to determine if the incoming request should be permitted.

If any permission check fails, a permissions denied exception will be raised, and the main body of the view will not run.

When this happens, either a "403 Forbidden" or a "401 Unauthorized" response will be returned.

### Object Level Permissions

REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

For performance reasons the generic views will not automatically apply object level permissions to each instance in a queryset when returning a list of objects

Custom permissions can also be implemented.

Third party permission packages are also available.

Notes taken from [DJANGO REST FRAMEWORK](https://www.django-rest-framework.org/api-guide/permissions/#object-level-permissions)