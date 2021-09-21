# APIs

1. What does REST stand for?

- Representational State Transfer

2. REST APIs are designed around a *resources*

3. What is an identifer of a resource? Give an example.

A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

 ```https://adventure-works.com/orders/1```

4. What are the most common HTTP verbs?

```GET, POST, PUT, PATCH, and DELETE```

5. What should the URIs be based on?

- should be based on nouns (the resource) and not verbs (the operations on the resource).

6. Give an example of a good URI.

``` https://adventure-works.com/orders  // Good ```

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

- its a bad thing, chatty" web APIs  expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires.

8. What status code does a successful GET request return?

``` code 200 (OK) ```

9. What status code does an unsuccessful GET request return?

```404 (Not Found)```

10. What status code does a successful POST request return?

```status code 201 (Created)```

11. What status code does a successful DELETE request return?

``` status code 204 (No Content) ```

### [resource](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design#what-is-rest)

## Things I want to know more about
