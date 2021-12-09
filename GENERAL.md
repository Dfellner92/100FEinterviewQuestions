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

### Web Pages

What happens when you hit enter after typing in a url on a browser? The URL is then used to find the server where the website is hosted and returns the dependencies. Authentication could play a part in this process. Once granted access, the index page will fire off dependencies such as image sources, javascript pages, or style sheets.

### Recursion

Recursion is when you have a function that calls itself until it no longer can, then returns a value that is typically some type of combination of the returns of each call. 

### OOP

Object oriented programming is a type of programming procedure for structuring our code. It allows us to have an object and class structure to encapulate our logic, which includes private and public methods; from there we can abstract our classes and showcase what we want the user to see and what we dont. Another key piece of OOP is inheritence, where, similar to dependency injection, new classes can inherit some traits from another class, which allows for code not to be redone. 

### Functional Programming

Functional programming has 2 main objectives. One is pure functions, which operate the same way every time (there is nothing outside of the scope that would alter this). The other deals with state management, meaning the ability of a function to update a global variable or a state. 


### Components

- Recent editions of JS and HTML have added web components, however
- most times components are used will be in the context of a frontend framework such as react or vue
- the concept: you have HTML template that gets referenced by a tag name that youve defined.
- you can pass functions to these templates in their tags, or pass data in the form of state 
- The key to these components is their reusability.
- a "nav-tag" component could be used to design and handle the event of a navigation bar link, and it could be used for each tag

### Agile and Scrum

- Generally work in 2 week sprints
- Try to have a velocity based off the history, sometimes that is increased to meet goals.
- morning meet: stand up to share accomplishments previous day, try to listen to how we can help
- Make sure JIRA tickets are understood, and that the reasoning behind their point values is understood as well. 
- sprint reviews work to showcase what has been done, and how the team can improve. 