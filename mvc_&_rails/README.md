# MVC & Rails

[MVC Architecture Explained Through Cooking](http://www.rubybacon.com/mvc-pattern-explained/)
appears to be gone from the web, so I pasted it below from an offline resource that I have.


##MVC Pattern Explained Through Cooking

by Mark Brown, rubybacon.com<br>

![img1](https://docs.google.com/uc?id=0B9sJDpz93uClWnUxeGlsSFV6Y00)

The model view controller (MVC) design pattern has been around for a long time and is used with Rails as the web framework for Ruby, and with .Net MVC as the web framework with C# and VB.Net. One of the benefits of the MVC pattern is how it promotes the concept of separation of concerns. Separation of concerns is the idea of keeping the actions, behaviors and concerns of each logical piece of an application in its own partition.

I am going to use the example of cooking to illustrate separation of concerns in the MVC pattern. If you think of the MVC pattern in terms of cooking, the model would be your fridge, the controller would be the chef in the kitchen, and the view would be the plate.

In a restaurant, a diner will request a meal to eat. The waiter then gives the order to the chef. The chef works on preparing the meal by gathering the ingredients from the fridge, prepping them, and then combining and cooking them. The prepared meal is then put on a plate and presented to the diner. The diagram below helps illustrate this.

![img2](https://docs.google.com/uc?id=0B9sJDpz93uClOUE4cGZRd2ZYOWs)

In an MVC web application, a user will request a page to view. The web browser gives the request to the server which directs it to the appropriate controller. The controller prepares the page to be viewed by gathering data from the model, prepping, sorting, and massaging the data for the page. The data is put on the page and the page given to the user. The diagram below helps illustrate this.
![img3](https://docs.google.com/uc?id=0B9sJDpz93uClVjY4eDlFYVZ4cTQ)

In both of the examples provided, each piece had a job to do, and that job was only done by that piece. The web server doesn’t get data from the model just like the waiter doesn’t get ingredients from the fridge. This separation of concerns allows for a more concentrated effort on each job, easier debugging and testing, and easier replacement for each piece, such as trading the fridge out for a freezer in a kitchen, or a database for a web service in as the model.
***

Another good article: [Getting Started with MVC](http://www.sitepoint.com/getting-started-with-mvc/)
