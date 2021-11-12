### speeding up a slow app

You could use the lighthouse tool against it to get a full report of the app, including a performance score. The audit will even provide a list of suggestions to make. You could also check the size of the network calls to see if anything, such as the size of an image, can be reduced.

### Dependency Injection

A dependency injection includes the creation of a service or a dependency (such as in a React or Angular app) that can then be injected into a the rest
of your code. If you were to create a service that called an API, that could be used in various other parts of your class component by passing it in as argument (after import) to your constructor.

### SOLID PRINCIPLES - Single Responsibility Principle

A class should only have one reason to change. Some easy ways to overlook applying this principle is if a url is added in dynamically when it could be written in as a constant, or there's a boolean passed in that tells the class to behave in one of two ways.

### SOLID PRINCIPLES - Open Closed Principle

If we were to modify the code, would the entire thing break apart? Or be hard to avoid adding a bug? You want the code to be open to expansion as well.

### SOLID PRINCIPLES - Liskov Substitution Principle

Don't try to force a child parent relationship between inheritence of objects if there is none. If you can't substitute the child for the parent, you've probably broken this rule.

### SOLID PRINCIPLES - Interface Segregation Principle

Make sure to modularize your objects, break them out piece by piece.

### SOLID PRINCIPLES - Dependency Inversion Principle

Using an interface to inject a service so that your code could be based on it.

### Conflict

My first sql-backend fullstack web app that I built was with a group of 3 other people during my fullstack bootcamp. There was one person in our group who had come into the bootcamp very well versed in programming. While this was helpful in many regards, he also got into the habit of accepting his own PRs and then explaining what he did only when we next met. Nobody spoke out about this for a few days, so I asked him if he'd be willing to wait to explain stuff to us before he went ahead with the PR.

### Debugging

There are several ways to debug your code. Using the browsers inspector gives access to the network to examine requests, the console to see which console methods are being applied, as well as the elements which can show if an attribute is being applied to an element or not.

There is also writing unit tests to tell if something has broken along the way. In react, these tests can be executed with the jest testing library to show if a component behaves as it should.

###
