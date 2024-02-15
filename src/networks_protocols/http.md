# 🔗 HTTP

**H**yper**T**ext **T**ransfer **P**rotocol is the foundation of data communication on the World Wide Web.

HTTP outlines how messages are formatted and transmitted, and how web servers and browsers should respond to various commands.

## History

HTTP was developed by Tim Berners-Lee at CERN in 1989, and it was first implemented in 1990.
It is a request-response protocol, which means that a client sends a request to the server, and the server responds with the requested data.

## Structure

HTTP is a stateless protocol, meaning that the server does not keep any data between two requests.
Each request from the client to the server must contain all the information required by the server to fulfil the request.

### Request

A request is made up of the following components:

- **HTTP Version**: The HTTP version specifies the version of the protocol being used.
- **Method**: The method specifies the type of request being made (e.g., GET, POST, PUT, DELETE).
- **URL**: The URL specifies the location of the resource being requested.
- **Headers**: The request can contain any number of headers, which are key-value pairs that provide additional information.
- **Body**: The body of the request contains the data that is being sent to the server.
