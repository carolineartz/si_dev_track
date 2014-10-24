# What the Web Does & How it Works

> At its core, our apps are just trading some text for some other text; a verb, path and maybe some data for a status, headers and a body

![World Wide Web Standards](https://docs.google.com/uc?id=0B9sJDpz93uClNXYtclNpVmFWLTg)

## How Client Requests Work

>This protocol specifies how two machines share information, which is called a request

The **Hypertext Transfer Protocol** (http) specifies how a **client machine** *requests information or actions* from **servers**.

- User issues a command
- Client generates a request
- Sends it to a Server and waits
- Server generates a request
- Server sends it to the client via the open connection
- Server hangs up
- Client renders to the user

**Note**: *The cycle is always initiated by the client, not by the server. The server cannot transmit unless the client has sent it an HTTP request message*.


![](https://docs.google.com/uc?id=0B9sJDpz93uClN19uamk0TFZpaDA)


## RECAP
- The web uses a client-server model.
- A client, which could be a web browser, a script, an application, or anything else, makes an HTTP request to a server.
- The request includes the HTTP method, path, headers, and a body.
- The method indicates the type of action to be performed, the path indicates what the resource being accessed is, the headers include extra information (like format or authentication), and the body includes information like the contents of a form submission.
- The server receives the request and returns a response.
- The response includes a status, headers, and a body. The status tells the outcome of the request (such as success or not found), the headers include extra information (like format or url to redirect to), and the body includes the actual content of the response (like the HTML and CSS).

***

[Read ME! - Awesome Resource for HTTP Resquests in Rails Apps](Back to Basics: HTTP Requests in Rails Apps)
