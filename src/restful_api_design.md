# RESTful API design

## What is REST?

REST or **Re**presentational **S**tate **T**ransfer, is an architectural style for designing networked applications.
It is designed to create APIs that are efficient, maintainable, and scalable.
It relies on a stateless, client-server, cacheable communications protocol — in virtually all cases, the HTTP protocol.

## RESTful API design principles

### 1. Client-Server

The client-server architecture is a computing model in which the server hosts, delivers and manages most of the resources and services to be consumed by the client.

### 2. Stateless

Each request from a client to a server must contain all the information required by the server to fulfil the request.
The server cannot store anything about the state of the client.

### 3. Cacheable

Cache constraints require that the data within a response to a request be implicitly or explicitly labelled as cacheable or non-cacheable.

### 4. Layered System

A client cannot ordinarily tell whether it is connected directly to the end server, or to an intermediary along the way.

### 5. Uniform Interface

The uniform interface between clients and servers simplifies and decouples the architecture, which enables each part to evolve independently.

### 6. Code on Demand (optional)

REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts.

## RESTful API design best practices

### 1. Use nouns instead of verbs

Use nouns to represent resources, and avoid using verbs.
For example, use `/users` instead of `/getUsers`.

### 2. Use plural nouns

Use plural nouns for consistency and to make the API easier to understand.
For example, use `/users` instead of `/user`.

### 3. Use sub-resources for relations

Use sub-resources to express relations between resources.
For example, use `/users/{userId}/posts` instead of `/posts?userId={userId}`.

### 4. Use HTTP methods

Use HTTP methods (GET, POST, PUT, DELETE) to operate on the collections and elements.
For example, use GET `/users` to get a list of users.
And use GET `/users/{userId}` to get a specific user.

They should follow CRUD (**C**reate, **R**ead **U**pdate **D**elete) operations:

- `GET` to retrieve a resource.
- `POST` to create a resource.
- `PUT` to update a resource.
- `DELETE` to remove a resource.

### 5. Provide filtering, sorting, and pagination

Use query parameters for filtering, sorting, and pagination.

### 6. Handle errors gracefully

Use standard HTTP status codes to indicate the status of the operation.

### 7. Version your API

Version your API to ensure that changes to the API do not break existing clients.
