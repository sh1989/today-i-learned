# Post Form Data with CURL

I was building a login route for a server, and rather than build a full front-end or use Postman, I used the following CURL command:

```
curl -X POST <url> -d "formParam1=value&formParam2=value2
```

For my use case, this returned the body of the response:
> {"id":1,"name":"Sam Hogarth","username":"sam"}

It's also possible to add the `-i` option to show all the response headers if so desired

In depth:
* `-X` specifies the request command to use
* `-d` specifies the HTTP post data
* -`i` includes the response headers in the output
