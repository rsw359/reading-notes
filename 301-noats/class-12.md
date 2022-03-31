# Class 03 *Reading Notes*

## Status codes

 ##Each status code represents:

100’s = Informational status codes(usually pertaining to header)
200’s = Success codes(request accepted)
300’s = Redirection codes(resource has moved)
400’s = Client error codes (invalid request; incorrect input)
500’s = Server side error codes(server problems)

What is a status code 202?
 *Accepted*

- With asynchronous processing, this code tells the client that the request was valid, but its processing has not finished yet

What is a status code 308?
*Permanent Redirect*

- Tells the client to use another URL to access the resource and not use the current URL anymore

What code would you use if an update didn’t return data to a client?

- 204 No Content

What code would you use if a resource used to exist but no longer does?

- 410 Gone - This is like 404 but we know that the resource existed in the past, but it got deleted or somehow moved, and we don’t know where.

What is the ‘Forbidden’ status code?

- 403 Forbidden - The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.
