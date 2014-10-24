# Request Response: Rails

![diagram](https://docs.google.com/uc?id=0B9sJDpz93uClcmFVSm9NZmQ4Unc)
[ref](http://tutorials.jumpstartlab.com/topics/routes/request_cycle.html)

Understanding the Rails Request/Response cycle will help you determine where to write teh different parts of code that makeup your application.

## Router/Dispatcher

The router is the front line of our application. It receives the request information from the web server and, based on that information, decides which controller action should be called. Rails applications, following the REST pattern, allows the router to make its decision based on two components: **the verb and the path**.

The router relies on a "**routes table**" which you configure. It matches the request against the table and then triggers the corresponding controller action.

## Controller

The controller coordinates between the model and the view, but it should do as little actual work as possible. It receives the parameters from the router, passes them on to appropriate model methods, then feeds the results to the view layer.

**Beware**: Controllers are where the average Rails programmer goes wrong. **An action should have very little intelligence and almost no "business logic", those responsibilities belong elsewhere**. We’ll see how to build actions following this premise in the Controller section.

## Model

*Persistence and business logic should all live at the model layer*. It’s been said that "the model is where real programming happens." When we deal with models we’re working in plain Ruby, building up the tools that the rest of the app can use to access and manipulate data.

## Views

Data flows up from the model through the controller to the views. *The views are responsible for mixing presentation code (HTML, CSS, JavaScript) with application data*. You should avoid any business logic in views.

[ref](http://tutorials.jumpstartlab.com/topics/routes/request_cycle.html)
