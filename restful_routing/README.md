# RESTful Routing

## REST: REpresentational State Transfer
> a pattern described by Roy Fielding in 2000. It describes a simple model of interacting with "resources" on the web

- describes resources (in our case URLs) on which we can perform actions.
- A RESTful application programming interface (API) exposes its data as resources (or nouns) at URIs that clients interact with via HTTP methods like GET and POST.

<br>
<table>
  <tr>
    <th colspan="3">7 RESTful actions</th>
  </tr>
  <tr>
    <td>GET</td>
    <td>index</td>
    <td>(list)</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>new</td>
    <td>(the page from which you can create)</td>
  </tr>
  <tr>
    <td>POST</td>
    <td>create</td>
    <td></td>
  </tr>
  <tr>
    <td>GET</td>
    <td>show</td>
    <td></td>
  </tr>
  <tr>
    <td>GET</td>
    <td>edit</td>
    <td>(the page from which you can update)</td>
  </tr>
  <tr>
    <td>PATCH/PUT</td>
    <td>update</td>
    <td></td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>destroy</td>
    <td></td>
  </tr>
</table>

<br>

### Resources for Rails RESTful routing
[Rails Guides-Routing from the Outside In](http://guides.rubyonrails.org/routing.html)<br>
[Jumpstart Labs: The Rails Router](http://tutorials.jumpstartlab.com/topics/routes/router.html)


***
**Alternatives to REST?**

REST isn't the only pattern for resource interaction on the web.

A popular ASP.NET pattern is *remote procedure call* (RPC), which refers an API style where endpoints perform arbitrary actions, not necessarily tied to a particular resource. RPC service methods combine the noun and verb in one method name (e.g. GetPosts or SendInvoice).
***

