---
title: "Content Creation Phase: Creative Commons WordPress Theme Base Usage Guide"
date: 2020-11-18T01:24:54+02:00
tags: ["gsod"]
draft: false
---

For the past couple of weeks we have been actively creating content for the Creative Commons WordPress Base Theme Usage Guide. Currently the draft content is under final review before it is migrated to the main docs site.

## Our Strategy
Our main goal in creating the docs is to create rich, intuitive, engaging, and beautifully presented community facing documentation for the Creative Commons WordPress Theme Base. 

In alignment with the defined goal, our core focus is to create the docs collaboratively.

The CC WordPress team consists of I, Jacqueline Binya, [Hugo Solar](https://github.com/hugosolar) and [Timid Robot Zehta](). Although our team is small it is quite diverse. It consists of a diverse mix of technical skills: I am a junior developer whereas Hugo and Timid are way senior. We also have non-native and native English speakers.

Diversity is important as we hope to create a high quality product that caters for everyone.

My role as the tech writer/frontend developer is to create the content: write the documentation, build the docs site and also to create all illustrative media.

During the content creation phase, the first step involved creating the skeleton of the actual docs site. We created a git branch called _docs_ within the [creative-commons/wp-theme-base](https://github.com/creativecommons/wp-theme-base) repository. All content related to the documentation is persisted in that branch. So,please feel free to contribute. We then used [JamDocs](https://gridsome.org/starters/jamdocs/), a [Gridsome](https://gridsome.org/) theme to quickly scaffold the site. We had to adapt the theme so as to make it meet our own specific needs, this involved overhauling the styles and changing the functionality of some of the features in the theme. After that was completed, we then created a [Google Doc](https://docs.google.com/document/d/1yfAQGG70T8BUhZYWglAlQ_lTo4_tYpyjhPN5FsZnSvI/edit?usp=sharing) we use for collaboratively writing the draft content for the docs site.

## Tech Stack
As it was mentioned we used [Gridsome](https://gridsome.org/) a static generator for [Vuejs](https://vuejs.org/). We chose Gridsome because:

- We wanted to lower the barrier of entry to contributing:
    - Gridsome/Vuejs community is very active, help is but a click away.
    - The Gridsome official documentation is very resourceful and well maintained.

- Gridsome is highly flexible: The content for the actual documentation is written in [Markdown](https://www.markdownguide.org/getting-started/) but using [@gridsome/vue-remark](https://gridsome.org/plugins/@gridsome/vue-remark), which is a Gridsome plugin, we are able to use javascript in Markdown. We intend to include a copy to the clipboard Vuejs component in the site.

- Time Constraint: This project is a short running project which has to be completed in a 3 month period. Through the use of JamDocs, a Gridsome templating theme as well various plugins it was easy and fast to get started we were able to add more functionality to the theme with minimal effort.

- Ease of integrating [CC Vocabulary](https://cc-vocabulary.netlify.app/) with Gridsome: it is a requirement that the general aesthetics of all front facing Creative Commons applications is derived from the CC Vocabulary Design System. Major cons for using a design system include the ensuring uniformity in design for all front facing CC products.

## Tools Used
- [Figma](https://www.figma.com/):
![An example of an illustrative asset made on Figma](https://res.cloudinary.com/di70zcupa/image/upload/v1605656295/has-widgets_y3at9g.png)

Figma was used to make assets(banners, logos and illustrations) in the theme. The illustrative media was created with accessibility in mind and all the topography used in the illustrative assets was derived from the CC Vocabulary.

- [VokoScreenNG](https://linuxecke.volkoh.de/vokoscreen/vokoscreen.html): an open source screencast recording tool used to record all the screen cast demos available in the docs site.

- [ShortCut](https://shotcut.org/): an open source video editing tool.

## What comes next ?

After the final review is completed and all feedback implemented we will migrate all the content to the main docs site. 

_Stay tuned for an update about the launch of the CC WP Theme Base docs site._

