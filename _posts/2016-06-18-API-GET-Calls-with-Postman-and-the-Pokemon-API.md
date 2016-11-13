An application programming interface (API) is a set of routine definitions, protocols, and tools for building software and applications. A good API makes it easier to develop a program by providing all the building blocks, which are then put together by the programmer. [wikipedia](https://en.wikipedia.org/wiki/Application_programming_interface)

For this example we're going to use the [Pokemon API](https://pokeapi.co/). Open APIs, such as the Pokemon API, do not require developer keys or any other kind of authorization.

###Getting Started with Postman
**[Postman Docs](https://www.getpostman.com/)**

You can use the web-based or desktop version of Postman.

###Testing GET requests with Postman
From the Pokemon API documentation we know that our GET request needs to be in the following format: `https://pokeapi.co/api/v2/` followed by the parameters of your query, or the address of the information you want to GET with your call.

For example: `https://pokeapi.co/api/v2/pokemon/1/ `-- will return the information for the Bulbasaur pokemon.

The API docs provide the information you need to call other types of information -- the postman tool will help you validate the information that you are fetching and make sure that it is the information that you want before using the API call on a site, or in another capacity.

To try this on your own computer, make sure "GET" is showing in the upper left (if not select "GET" from the dropdown). Put the link `https://pokeapi.co/api/v2/pokemon/1/` into the text box to the right of the "GET" and then click on "Send"

![alt text](http://i.imgur.com/VW32ARA.png "Postman Screenshot")
