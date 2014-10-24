# The World Wide Web

## The Web vs The Internet

**The Internet**: The Internet has been around a lot longer than the Web. It is an interconnected system of networks that connects computers around the world via the *TCP/IP protocol*

**World Wide Web** (early 90s) The *I*nternet enables the to exist. The World Wide Web is the *complete set of documents residing on all Internet servers* that use the **HTTP protocol**. These documents are accessible through a web browser and can be navigated by using hyperlinks that have been implemented using **HTML (HyperText Markup Language)**.

>**The World Wide Web** is the web of interconnected pages and files that we are used to browsing today.

[the first page published on the Web](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/TheProject.html)

*ref*: [The Origin of the Internet and Hypertext](http://www.htmlgoodies.com/beyond/reference/article.php/3639741/The-Origin-of-the-Internet-and-Hypertext.htm)


## What it Does  & How it Works

> At its core, our apps are just trading some text for some other text; a verb, path and maybe some data for a status, headers and a body

![World Wide Web Standards](https://docs.google.com/uc?id=0B9sJDpz93uClNXYtclNpVmFWLTg)

### How Client Requests Work

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

#### Breaking down HTTP Request and Response

![](https://docs.google.com/uc?id=0B9sJDpz93uClN19uamk0TFZpaDA)

The first line of an HTTP request is called the **Request-Line**. It contains:

1. URI
2. Headers
3. Body
4. Method (verb/action)


##### URI: Uniform Resource Identifier

- how objects are identified.
- clients use URIs to tell the server what object to act on for a given request.
- a URI is really nothing more than a web address.

<br>
***
**TIDBIT:** *URI* vs *URL*?

A *Uniform Resource Identifier* (URI) is a compact sequence of characters that identifies an abstract or physical resource.

A URI can be *further classified* as a locator, a name, or both. The term *Uniform Resource Locator* (URL) refers to the subset of URIs that, in addition to identifying a resource, provide a means of locating the resource by describing its primary access mechanism (e.g., its network “location”).

[ref](http://danielmiessler.com/study/url_vs_uri/)
***

<br>
##### Request Header Fields

- where a client can communicate additional information to the server.
- e.g., information about the client, ie. what type of browser the request originated from
- these values can modify how the server responds to the request.

***
**RAILS REF**

the Content-Type header value is used by the Rails framework to decode a request’s message body.
***

##### Message Body
- send information to the server about the entity the client wants to modify or create.
- can be communicated using several different encoding mechanisms

> Note: Not all client requests are allowed to have message bodies.

##### Method (verb or action)
- Tells the server what the client wants it to do.
- There are many different methods available...

***
**RAILS REF**

The four HTTP request methods that are most relevant to Rails developers are: **GET**,  **POST**, **PATCH**, **DELETE**
***

- **GET** - how a client machine tells a server that it wants information about the item identified by the URI. Because GET requests are all about *asking for information*, they are **not permitted to have request bodies**. GET requests may submit data back to the server via the URI query string that looks something like this `?key2=value2&key2=value2`.

> Every time you are load a page you are making a GET request*.

*exception: pages that are an (html) form of type POST

- **POST** - POST requests send data via *request header*. POST requests are how a client tells a server to add an entity as a child of the object identified by the URI. The entity that the client expects the server to add is transmitted in the *request body*.

- **PATCH** - How a client tells a server it wants to modify an object identified by the URI the request is sent to.

- **DELETE** - How a client tells a server to remove an object identified by the URI the request is sent to.


## RECAP
- The web uses a client-server model.
- A client, which could be a web browser, a script, an application, or anything else, makes an HTTP request to a server.
- The request includes the HTTP method, path, headers, and a body.
- The method indicates the type of action to be performed, the path indicates what the resource being accessed is, the headers include extra information (like format or authentication), and the body includes information like the contents of a form submission.
- The server receives the request and returns a response.
- The response includes a status, headers, and a body. The status tells the outcome of the request (such as success or not found), the headers include extra information (like format or url to redirect to), and the body includes the actual content of the response (like the HTML and CSS).

