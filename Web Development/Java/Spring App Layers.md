**Spring App Layers:** Spring can be thought of having the architecture of these layers:
Presentation -> Service -> Persistence layer

**Persistence:** This layer handles interactions with the database. *What's in the layer:* Entities, Repositories / DAO.
**Service:** This layer uses all the functionality of the persistence layer to handle and execute any of the logic that we need to accomplish in our application.
**Presentation:** This layer uses all of the data from the service layer and expose it to the user. *Ex.* Graphql, WebSocket, RestAPI.

#backend #Web-Dev #java #spring 