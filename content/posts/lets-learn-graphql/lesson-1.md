---
title: "Intro to GraphQL"
date: 2020-09-23T16:32:17+02:00
tags: ['life', 'graphql']
draft: false
---

Well I have a huge announcement to make!
Wait for it...

<img src="https://media.giphy.com/media/xUA7b7pLM4w1edn0yI/giphy.gif" alt="Woman making gestures">

I am learning GraphQL 😱

I just finished my first tutorial on <a href= "" class="article-link">EDX</a>. I am pretty stoked about it, its something I have putting off for months mainly because of two reasons:
- I have been insanely busy and,
- I have been feeling overwhelmed lately about the ton of stuff I have to learn as a developer. When you hear people say as that _As a developer the learning never stops_, its not a cliche.

 But the good news is: I have since developed a strategy to deal with the anxiety of associated with handling a lot of work responsibilities whilst trying to maintain a healthy life balance. I now keep a calender to manage and track my work. I set up weekly goals which I then breakdown to small daily tasks which are achievable. Adjusting my attitude towards learning has been helpful as well, I have since reconciled with the fact that if I am serious about being a developer: consistently learning new things has to become part of my lifestyle. 
 
 Lastly one thing that I feel is even important to mention is that I practice a little kindness towards myself and I also have a reward system in place. So, am really looking forward to that holiday in Capetown🧳🐳👙.



 <a href= "https://www.edx.org/" class="article-link">EDX</a> is an online learning platform which offers a variety of university level courses. The EDX course are free but if you want certification you have to pay a fee.

I decided to document my notes as I am going through the <a href="https://courses.edx.org/courses/course-v1:LinuxFoundationX+LFS141x+3T2019/course/" class="article-link"> Exploring GraphQL: A Query Language for APIs
</a> course and share them.

 So here goes:
 
 ## Lets discuss how modern apps work

 <img  src="https://res.cloudinary.com/di70zcupa/image/upload/v1600877965/client-server_bpqr51.png" alt="Client server model">


 Modern apps are generally dynamic and robust. They make multiple network calls to fetch and display dynamic data. The data is usually stored in some remote database. The data stored within the databases is exposed through APIs. An API is an application programmable interface, basically that means it allows computers to communicate over the client server model. Now a server is simple a computer that is optimized to respond to queries.

 ## What is GraphQL ?

- It’s a query language for APIs
- It was created as an alternative to REST in 2015 by Facebook
- Enables declarative data fetching: client can explicitly specify what data they require from a server. The catch here is the specification has to be in a hierarchical structure.
- So essentially you set up a GraphQL server to handle queries, the graphql server exposes a single endpoint and that endpoint responds to all the queries
- GraphQL is generally more performant in than  REST


 ## Why GraphQL ?

- As the data used in applications became more detailed and complex its become cumbersome to query data using REST, GraphQL provides a clean and effective solution to query complex data. 
- GraphQL drastically reduces the number of network calls when transferring data between the client and the server so that makes it a good fit for use in areas with poor internet connectivity it’s also suited for users who use low power devices (with poor batteries repeated network calls deplete power fast)
- Increased mobile usage: GraphQl reduces the amount of data transferred over the network so applications running on mobile devices generally become more performant.
- In modern software development, we have a wide array of frameworks and platforms that run client applications, GraphQL standardizes how they query data.

_And we done, thank you for taking time to read my blog 🦥._
_Sale kahle👋_




