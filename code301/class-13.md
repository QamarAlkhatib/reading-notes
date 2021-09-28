# CRUD

1. In your own words, describe what each group of status code represents:

    * 100’s = they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.

    * 200’s = In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.


    * 300’s = This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location

 
    * 400’s =A client is sending incorrect input and should confirm the input parameters are correct before retrying the request.

 
    * 500’s = Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server.



2. What is a status code 202?

    * Accepted

3. What is a status code 308?

    * Permanent Redirect 

4. What code would you use if an update didn’t return data to a client?

    * 204 No Content 

5. What code would you use if a resource used to exist but no longer does?

    * 303 See Other 

6. What is the ‘Forbidden’ status code?

    * 403 Forbidden
    
---

## Things I want to know more about