# HTTP Request Detail
![Anatomy of HTTP Request](https://docs.google.com/uc?id=0B9sJDpz93uCld0tTVFBNN19KNHM)
[ref](http://binaryengineering.blogspot.com/2011/02/software-architecture.html)

The first line of an HTTP request is called the **Request-Line**. It contains:

1. URI
2. Headers
3. Body
4. Method (verb/action)


#### 1. URI: Uniform Resource Identifier

- how objects are identified.
- clients use URIs to tell the server what object to act on for a given request.
- a URI is really nothing more than a web address.

<br>
***
**TIDBIT:** *URI* vs *URL*?<br>
A *Uniform Resource Identifier* (URI) is a compact sequence of characters that identifies an abstract or physical resource.

A URI can be *further classified* as a locator, a name, or both. The term *Uniform Resource Locator* (URL) refers to the subset of URIs that, in addition to identifying a resource, provide a means of locating the resource by describing its primary access mechanism (e.g., its network “location”).

[ref](http://danielmiessler.com/study/url_vs_uri/)
***

<br>
#### 2. Request Header Fields

- where a client can communicate additional information to the server.
- e.g., information about the client, ie. what type of browser the request originated from
- these values can modify how the server responds to the request.

***
**RAILS REF**<br>
the Content-Type header value is used by the Rails framework to decode a request’s message body.
***

#### 3. Message Body
- send information to the server about the entity the client wants to modify or create.
- can be communicated using several different encoding mechanisms

> Note: Not all client requests are allowed to have message bodies.

#### 4. Method (verb or action)
- Tells the server what the client wants it to do.
- There are many different methods available...

***
**RAILS REF**<br>
The four HTTP request methods that are most relevant to Rails developers are: **GET**,  **POST**, **PATCH**, **DELETE**
***

- **GET** - how a client machine tells a server that it wants information about the item identified by the URI. Because GET requests are all about *asking for information*, they are **not permitted to have request bodies**. GET requests may submit data back to the server via the URI query string that looks something like this `?key2=value2&key2=value2`--see an example in detail below.

![Anatomy of a URL](https://docs.google.com/uc?id=0B9sJDpz93uClbEFKNU4xN2pyQzQ)

> Every time you are load a page you are making a GET request*.

*exception: pages that are an (html) form of type POST

- **POST** - POST requests send data via *request header*. POST requests are how a client tells a server to add an entity as a child of the object identified by the URI. The entity that the client expects the server to add is transmitted in the *request body*.

- **PATCH** - How a client tells a server it wants to modify an object identified by the URI the request is sent to.

- **DELETE** - How a client tells a server to remove an object identified by the URI the request is sent to.

Note: Browsers don’t actually implement all four verbs. Also, until recently, HTML forms only supported GET and POST. This leads to some complication...Rails to the rescue!

***
**RAILS REF**<br>
Rails circumvents these limitations by *faking* the request verbs using a `_method` parameter. If a POST request comes in with no `_method`, the router will consider it a POST. If a POST comes in with the parameter `_method` set to "delete", however, the router will consider it a DELETE.
***
<br>
