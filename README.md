### This is the client application that consumes properties from the centralized config-server

#### Assumptions
 1. There's a git repository that acts as the repo for all properties
 2. There's a centralized config server pointing to that repo
 3. Server is up and running for the client to consume those properties
 
#### Hacks
on fly changes can be made in the config repo(git repo) and accommodated in the client by simply using the activator end-point /actuator/refresh
> curl localhost:8080/actuator/refresh -d {} -H "Content-Type: application/json"