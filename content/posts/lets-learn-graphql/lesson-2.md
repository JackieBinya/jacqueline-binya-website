---
title: "GraphQL vs REST"
date: 2020-10-03T17:50:45+02:00
tags: ['graphql']
draft: false
---

Historically REST is the accepted standard for designing web APIs.

The main advantages of using REST were:
- REST is stateless meaning every server call is independent of any other network calls made to the server. The server will not persist any state about the queries it receives.
- It provides a structured way to query resources.

**The problem**
- REST was intended to be a strict specification used to design APIs but in reality, it was wildly interpreted: most APIs described as being Restful aren't really Restful, they don’t adhere to the strict specification
- REST APIs have shown to be too inflexible to keep up with the rapidly changing requirements on the client apps that access them.

**The Solution**
- GraphQL was designed to cope with the need for increased flexibility and efficient client-server interaction.

## Demo of  a query REST vs GraphQL
Say we have a blogging application, such that for each blogger’s page:  we render the blogger’s name, titles of their posts, and their latest three followers. As shown below:
![Example Blog](https://res.cloudinary.com/di70zcupa/image/upload/v1601742427/example-blogging-app_xorm3b.png)

### Using REST
- Typically several network calls are made by the client to the server at different endpoints:
   - _/users/< id >_
   - _/users/< id >/ posts_
   - _/users/< id >/ followers_
- The client app is constantly downloading the resources which are not required, so the user’s data is wasted. For instance it fetches all the user data eg email, age, lastname, birthday, etc. when a network call is made to _/users/< id >_.  
- The most simple and obvious solution would be to design our API such that it only exposes the data they required by the client. But the problem is that in modern app development, you need to iterate quickly, constantly redesigning your API can be a huge drawback time-wise. 

### Using GraphQL
- In a graphql server you only have a single endpoint that can be used by different clients who want to retrieve data from the database.

![Typical GraphQL Post Request](https://res.cloudinary.com/di70zcupa/image/upload/v1601750016/typical-gql-post_huyn9z.png)

**How it works:**
- You make a post request to the Graphql server
- In the post request body, you include the query 
- The query contains all the data requirements of the client.
- The graphql processes the request and manipulates the database and then sends a response which is JSON object.

**Differences between Rest and GraphQL**
- Eliminate the problem of Overfetching and Underfetching:
    - _Overfetching_: Describes a scenario that happens when querying a Restful server and we end up downloading unnecessary data into our app.
    - _Underfetching_: The response to the query made to a specific endpoint returns insufficient data that the client has to make  (n+1) requests just to get sufficient data.

- Graphql allows for low-level monitoring of the requests made to the server. It uses resolver functions to resolve queries made by the client. These can be monitored so as to analyze the application.
- GraphQL uses a strong type system once types are described in the schema the frontend developers can mock an API and continue working on the client-side whilst the backend engineers continue to build the backend.

> All the images used in this blog article were part of the <a href="https://courses.edx.org/courses/course-v1:LinuxFoundationX+LFS141x+3T2019/course/" class="article-link"> Exploring GraphQL: A Query Language for APIs</a> course.