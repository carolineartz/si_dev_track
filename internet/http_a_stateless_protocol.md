# HTTP is a Stateless Protocol

>**Stateless**: Each request from a user for a Web page or URL results in the requested pages being served, but without the Web (HTTP) server remembering the request later. In other words, there is no recorded continuity. Each communication is discrete and unrelated to those that precede or follow.
<br>

In a purely stateless environment, each request would contain all the information the server would need to process. But, many applications need to maintain state to keep track of user authentication to view certain content or to keep track of what a user is doing. We wouldn’t want to send user credentials over the wire for each request.

So, how is state information maintained?


### Cookies
Web browsers provide an area in their sub-directories where state information can be stored and accessed. The area and the information that Web browsers and server applications put in this area is called a cookie.


### Sessions
Imagine a request over the web where you have a client browser communicating to a server process. To maintain state over the stateless http protocol the browser typically send a **session identifier** to the server on each request. For each request the server will be like “ah, its this guy”. State information can then be looked up in server side memory or in a database based on this session id.

- Cookies are unique to client (browser) & domain
- Domains don't see cookies for other domains
- sessions depend on cookie to maintain some state
- as little as session ID or as mich as entire session's data

[ref](http://sethuramanmurali.wordpress.com/2013/07/07/stateful-stateless-cookie-and-session/)
