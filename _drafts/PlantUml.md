---
layout: post
title: 
---

Hi, this time I would like to share with my recent finding - [PlantUml](http://plantuml.com)

# PlantUml

PlantUml is an markup language designed to draw UML diagrams. 
Just look on example: 

```plantuml

@startuml


package "Some Group" {
  HTTP - [First Component]
  [Another Component]
}
 
database "MySql" {
  
}


[Another Component] - HTTP
[Another Component] --> MySql


@enduml
```

Would be rendered as: 

![result](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3XSNLq5YSdPYUgg2Kd1-Rgg2Ur5-QO6IGZMNWe97I4Y0Wgv2j5jcKN69WdD-Ra5-NcfUIInGAjenBxya8xK8MRIMIu4h9R4aCIcn66YORsLmOGx47A0C5nSM7K2pGLPWbzArKm0R0TJga9gN0dGgG8010000)

In case of simple class diagrams it could be also rendered as ascii text:

```plantuml

@startuml

title Classes - Class Diagram


class Dwelling {
  +Int Windows
  +void Lock()
}

class Apartment
class House
class Commune

Commune --> Apartment

@enduml
```

ascii: 

```
,------------.                     
|Dwelling    |  ,-------.   ,-----.
|------------|  |Commune|   |House|
|+Int Windows|  |-------|   |-----|
|------------|  |-------|   |-----|
|+void Lock()|  `-------'   `-----'
`------------'       |             
                     |             
                     |             
               ,---------.         
               |Apartment|         
               |---------|         
               |---------|         
               `---------'         
```


# Use with Markdown

If you like to insert your new shiny uml diagram have inserted into Markdown page, you have to options: 

Render the image, upload to your graphic assets directory and simple link it: 

```
![your uml](/assets/uml.png)
```

However above method would obviously work, but is not especially efficent. When you like to change anything in the diagram to make it updated, it would
be necessary to render image and upload it again. 
Other option is to use [planttext.com](http:planttext.com) online editing tool instead, it gives you possibility to encode your uml into url like:

```
![result](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3XSNLq5YSdPYUgg2Kd1-Rgg2Ur5-QO6IGZMNWe97I4Y0Wgv2j5jcKN69WdD-Ra5-NcfUIInGAjenBxya8xK8MRIMIu4h9R4aCIcn66YORsLmOGx47A0C5nSM7K2pGLPWbzArKm0R0TJgagN0dGgG8010000)
```


# Use with Gists


# Place in GitHub Readme.md

# Resources

* [plantuml.com](http://plantuml.com/) - main page, all you need to know about PlantUml
* [this blog](https://rdmueller.github.io/plantuml-gradle/) - some interesting articles and tricks 
* [planttext.com](planttext.com) - plantuml online editor
* [PlantUml Gits](http://uml.mvnsearch.org) - renders plantuml from github 
