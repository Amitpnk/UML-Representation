# UML-Representation
 Sample UML represtation

## What is UML?

* Unified Modeling Language, a standard language for designing and documenting a system in an object-oriented manner.

* Communicating language between technical architects and developers

* Diagram also express design of a software achictecture

* It has few diagram which is explained below
    * Activity Diagram
    * Use case diagram

### Activity Diagram

Activity diagram used to capture complicated process flows in project

![Activity Diagram - Check for admin profile](Assets/ActivityDiagram.png)  

Copy below code in http://www.nomnoml.com/

``` nomnoml
[<frame>Check Admin login |
[<start>st]->[Login]
[Login]->[<choice>Check if User is Admin]
[Check if User is Admin] yes ->[Redirect to admin page]
[Check if User is Admin] no ->[User page]
[Redirect to admin page] yes ->[<end>e]
[User page] no ->[<end>e]
]
```

### Use case diagram

Use case diagram has divided to 3 types
* Scenario
* Actor
* Use Case

Actor is two types
* Primary (Simple user)
* Secondary (Admin user)

Include and Exclude deines relationship between use case

![Usecase Diagram - Check for admin profile](Assets/UseCaseDiagram.png)  

Copy below code in http://www.nomnoml.com/

``` nomnoml
[<frame>Use case diagram |
[<actor>Simple user] - [Add simple Customer]
[<actor>Admin user] - [Add Discount Customer]
[Add Discount Customer] <extend> --> [Add simple Customer] 
[Add simple Customer] <include> -> [<usecase>Send notification] 
[Add Discount Customer] <include> -> [<usecase>Send notification] 
]
```

### Class diagram

Class diagram is our prototype which helps us to create objects

![Class Diagram](Assets/ClassDiagram.png) 

Note: 
* public +
* private -
* protected #
* Abtract class {}
* Interface <<>>

Copy below code in http://www.nomnoml.com/

``` nomnoml
[Customer]--:>interface[<<ICustomer>>|+Add()]
[Customer|+CustomerCode: int;-CustomerName: nvarchar(100);#CustomerName: nvarchar(100)|+Add();-Validate()]
[GoldCustomer|+Discount()]-:>[Customer]

[<abstract>{Engine}||start()]
```

