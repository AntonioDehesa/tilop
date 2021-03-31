# API
**Application Programmable Interface**
Programmatic interface consisting of one or more publicly exposed endpoints to a defined request-response message system exposed via HTTP based server. 
Set of tools for programmers. 
Nowadays, when someone mentions API, they refer to Web APIs, but there are other types. 
## How do they help
APIs work as some kind of *middle-man*, allowing different applications to interact with each other. For example, if you wanted to create an app that shows something on the map, you would not create your own map system, and launch satellites, and cars to take photos, and whatever. You would most likely use the Google Maps API. This way, you dont have to know how these maps are created or how they work, you just need to know how to interpret the information it gives you back. 
Another advantage is the usage of remote APIs. 
This way, you can use implement big and slow processes in your app, or web app, while the heavy load is done somewhere else. 
For example, how shazam works. You record a piece of a song in your phone, and shazam tells you its name. 
But that process was not done directly in your phone. The recording is sent to a remote server with an API, and it gives you back the name of the song. Without it, you would need massive amounts of computational power on your phone, and to store every song on it. 
## REST
Representation State Transfer. 
APIs that meet the REST architectural constraints are considered to be RESTful. 

## REST architectural constraints
### Client-Server Architecture

The model is very simple: There is a client, and there is a server. 
The client makes the requests, and the server takes these requests, and returns an appropiate response. 

### Statelessness

HTTP protocol is stateless, meaning that it does not remember anything from previous requests or sessions. Want it to remember? You´ve got to send what you want it to remember with each request.

### Layered System

A layered system means that you might launch a request on server a, store the data on server b, and authenticate on server c. 
Components of a REST system cannot see beyond their own layer. 

### Cacheability

A RESTful API should support cacheability, using values such as "Last modified on". 
This way, we dont need to make unnecesary requests. 

### Uniform design



### Code on Demand

## CRUD
Acronym that stands for Creating, Reading, Updating, Deleting. 
Most of the resources in an app can do at the CRUD actions. 
