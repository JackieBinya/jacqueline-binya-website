---
title: "Implement hover on parent element trigger css effects on child element functionality in Vuejs"
date: 2020-12-16T17:53:20+02:00
draft: true
---

<img src="https://media.giphy.com/media/hFIq9i5y2H10Q/giphy.gif" alt="Santa Claus" >

Its the holidays of-course, but I am busy working on my portfolio. No rest for a junior developer until we bag that remote dev position. 

Lately I have been challenging myself to be more productive and try working on portfolio projects which require more technical skill. So, I am currently working on a [Todoist](https://todoist.com/) clone using Vue 2.
Yes I know, I would rather be using Vue 3 but at the moment most npm/yarn modules do not have support Vue 3 yet.

I came across a very peculiar and interesting problem as I was trying to style the navigation bar of my web app.

## The problem:
In the video that is embedded below, we have a simple navigation bar built using Vuejs. It has two menu items which are namely _Item One_ and _Item Two_. _Item Two_ has two sub menu items which are namely _Sub Menu 1_ and _Sub Menu 2_.
We want to emulate the functionality of _Item Two_ such that when you hover over _Item Two_  the sub menu becomes visible so you can navigate to the sub menu items and even click them to be redirected to a new page.But in the event that leave _Item Two_ or any of its sub menu items the sub menu disappears.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KTGg4pxiRBI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>