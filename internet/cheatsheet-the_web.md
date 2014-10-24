# Cheatsheet-The Web
HTTP stands for Hypertext Transfer Protocol.

HTTP uses a client-server model, where a client sends a request, and a server provides a response. Web browsers are clients.

A request includes a method (also called a verb), a path, headers, and a body:

Methods indicate the the type of action.
The path is the URL, like http://www.epicodus.com/students.html.
Headers include optional information, like format or authentication.
The body includes information like the contents of a form.
Common HTTP methods:

GET retrieves information without changing anything on the server.
POST creates something.
PATCH or PUT updates.
DELETE destroys.
Responses include status, headers, and body.

The status is a three-digit code that represents the outcome of the request.
Headers might include content type or redirect location.
The body includes the actual HTML, CSS, JavaScript, etc.
Common statuses:

200 OK (successful)
201 Created
301 Moved Permanently
302 Moved Temporarily
400 Bad Request
403 Forbidden (it exists but you aren't allowed to see it)
404 Not Found
422 Unprocessable Entity (you put in bad data)
500 Internal Server Error
502 Bad Gateway (the server sent the request to another server and got an invalid response)
503 Service Unavailable (the server is overloaded or down for maintenance)
