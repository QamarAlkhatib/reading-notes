# Permissions

Before any other code is allowed to run, permission checks are always conducted at the very beginning of the view. Permission checks usually use the authentication information in the request.user and request.auth attributes to decide whether or not the incoming request should be allowed.

Permissions are used to allow or prohibit access to various areas of the API to different types of users.

Allowing access to any authenticated user and denying access to any unauthenticated user is the most basic type of permission. This relates to the REST framework's IsAuthenticated class.

Allowing full access to authenticated users but only read-only access to unauthenticated users is a significantly less severe kind of permission. This relates to the REST framework's IsAuthenticatedOrReadOnly class.

## How permissions are determined

Permissions are always defined as a list of permission classes in the REST framework.

Each permission in the list is checked before the main body of the view is run. An exception is thrown if any permission check fails. Exceptions or PermissionDenied The view's main body will not run because of the NotAuthenticated exception.

When the permission checks fail, the response will be either "403 Forbidden" or "401 Unauthorized," depending on the rules:

- The request was authenticated properly, however authorization was denied. — The response code will be HTTP 403 Forbidden.
- Because the highest priority authentication class does not use WWW-Authenticate headers, the request was not successfully authenticated. — The response code will be HTTP 403 Forbidden.
- The request was not successfully authenticated, despite the fact that WWW-Authenticate headers are used by the highest priority authentication class. — An HTTP 401 Unauthorized response will be sent, along with the relevant WWW-Authenticate header.

## Object level permissions

Object-level permissioning is also supported by the REST framework. Permissions at the object level are used to determine whether a user should be authorized to act on a certain object, which is usually a model instance.

When.get object() is used, the REST framework's generic views handle object level permissions. There are exceptions, just as there are with view level permissions. If the user is not allowed to act on the specified object, the PermissionDenied exception will be thrown.

You'll need to explicitly execute the.check object permissions(request, obj) function on the view at the point where you've obtained the object if you're developing your own views and want to impose object level rights, or if you override the get object method on a generic view.

If the view has the appropriate rights, this will either raise a PermissionDenied or NotAuthenticated exception, or just return.

## Limitations of object level permissions

When returning a list of objects, the generic views will not automatically apply object level rights to each instance in a queryset for speed reasons.

When employing object level permissions, you'll often want to filter the queryset appropriately to ensure that users only see instances that they have permission to see.

Object level permissions from the has object permission() function are not applied when creating objects since the get object() method is not called. You must either implement the permission check in your Serializer class or override the perform create() method of your ViewSet class to restrict object creation.

---------

## API Reference

- AllowAny: Regardless of whether the request was authenticated or not, the AllowAny permission class will grant unfettered access.

This permission isn't technically required because you may get the same result by setting the permissions to an empty list or tuple, but you might find it handy to specify this class because it makes the goal apparent.

- IsAuthenticated: The IsAuthenticated permission class will refuse access to any user who is not authenticated, but will grant access otherwise.

This permission is appropriate if you only want registered users to have access to your API.

- IsAdminUse: If user.is staff is True, the IsAdminUser permission class will deny any user permission until user.is staff is False, in which case permission will be granted.

This permission is appropriate if you only want a small group of trusted administrators to have access to your API.

- IsAuthenticatedOrReadOnly: Authenticated users will be able to make any request using the IsAuthenticatedOrReadOnly method. Unauthorized users will only be able to make requests if they use one of the "safe" methods, such as GET, HEAD, or OPTIONS.

This permission is appropriate if you want anonymous users to be able to read your API but only authenticated users to be able to write it.

- DjangoModelPermissions:

Django's standard django.contrib.auth model permissions are used by this permission class. Only views with a.queryset property or a get queryset() function can use this permission. Only if the user is authenticated and has the appropriate model permissions will authorization be granted.

POST requests necessitate the user having the model's add permission.
The user must have change permission on the model to make PUT and PATCH requests.
DELETE requests necessitate the user having the model's delete permission.

To accommodate specific model permissions, the default behavior can be changed. For GET requests, for example, you might want to add a view model permission.

Override DjangoModelPermissions and set the.perms map attribute to utilize custom model permissions. Details can be found in the source code.
