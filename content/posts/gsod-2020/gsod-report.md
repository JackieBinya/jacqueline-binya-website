---
title: "My Google Season of Docs(GSOD) experience in a nutshell "
date: 2020-12-03T05:28:31+02:00
tags: ["gsod"]
draft: false
---


> A GSOD-2020 project report prepared by Jacqueline Binya on 29 November 2020

During the Google Season of Docs (GSOD) 2020, I contributed to the Creative Commons' _WordPress base theme usage guide_ project.

<a href="https://github.com/creativecommons/creativecommons-base" class="article-link">Creative Commons (CC) Base</a> is a universal WordPress Theme used to build front facing websites for CC. My role as a technical writer was to create community facing documentation for the CC Base theme collaboratively with the engineering team.

This involved creating the content for the docs, creating all illustrative media and also building the site used to host the documentation.

## Planning - Community Bonding phase

During the GSOD - Community Bonding phase, I had a meeting with my mentor Hugo Solar in which we strategized on how to effectively build the docs: this included refining and polishing up the project's objectives and action plan based off the <a href="https://docs.google.com/document/d/1XmIsMTLstbhRRSaNFP538YOXJiS0G5QrN6EzuqJfRy4/edit" class="article-link">proposal</a> I submitted for my GSOD application and also, establishing a workflow for doc development.

We decided to:
- Create a <a href="https://docs.google.com/document/d/1XmIsMTLstbhRRSaNFP538YOXJiS0G5QrN6EzuqJfRy4/edit?usp=sharing" class="article-link">Google Doc</a> to persist all the draft content which was accessible to all the team members
- Create a <a href="https://docs.google.com/document/d/19FYiB3zVo86_I7os7sO6ZHyZf8eN17x6OFq3WqxDQYY/edit?usp=sharing" class="article-link">tracker document</a> to manage and evaluate progress.
- I prepared <a href="https://www.figma.com/file/roAl4FwMwFQHhSDHpm9rk5/CC-WP-theme-frame?node-id=0%3A1" class="article-link">wireframes</a> for the docs site.
- We chose a documentation tool we wanted to use to build the docs site.

## We Create the Docs - Content Creation

To build the docs site we used <a href="https://gridsome.org/starters/jamdocs/" class="article-link">JamDocs</a> a <a href="https://gridsome.org/" class="article-link">Gridsome</a> theme. We had to adapt the theme: JamDocs, so as to make it meet our own specific needs, this involved overhauling the theme's default styles and also, changing the functionality of some of the features in the theme.

With regards to the doc development process: Its important to mention that the GSOD spans for 13 weeks and in the <a href="https://docs.google.com/document/d/1XmIsMTLstbhRRSaNFP538YOXJiS0G5QrN6EzuqJfRy4/edit" class="article-link">proposal</a> each week's expected deliverables are outlined. So to develop the docs for each week we would start off with a team meeting to discuss the content for the section we were working on that particular week, then next I would create draft content in a Google Doc during the course of the week. My mentors would then review the draft and suggest changes asynchronously, then I would then implement feedback gathered. Once the draft content was approved I then would migrate it to the docs site.

The mentors were readily available to answer questions on various communication channels and promptly gave me the assistance I required.

The codebase for the documentation of CC Base theme is available in the <a href="https://github.com/creativecommons/wp-theme-base" class="article-link">creative-commons/creativecommons-base</a> repository on Github, in a git branch called _docs_. All content related to the documentation is persisted in that branch.

### Tech Stack
As it was mentioned we used Gridsome a static generator for <a href="https://vuejs.org/" class="article-link">Vuejs</a>. We chose Gridsome because:

- We wanted to lower the barrier of entry to contributing:
    - Gridsome/Vuejs community is very active, help is but a click away.
    - The Gridsome official documentation is very resourceful and well maintained.

- Gridsome offers support for [Markdown](https://www.markdownguide.org/getting-started/) (a markup language) through plugins, all the content pages in the site are written using Markdown.

- Time Constraint: This project is a short running project which has to be completed in a 3 month period. Through the use of JamDocs, a Gridsome templating theme as well various plugins it was easy and fast to get started. We were able to add more functionality to the theme with minimal effort.

- Ease of integrating <a href="https://cc-vocabulary.netlify.app/" class="article-link">CC Vocabulary</a> with Gridsome: it is a requirement that the general aesthetics of all front facing Creative Commons applications is derived from the CC Vocabulary Design System. Major cons for using a design system include ensuring uniformity in design for all front facing CC products.

### Tools Used

- <a href="https://www.figma.com/" class="article-link">Figma</a>:
Figma was used to make assets(banners, logos and diagrams) in the theme. The illustrative media was created with accessibility in mind and all the topography used in the illustrative assets was derived from the CC Vocabulary.

- <a href="https://linuxecke.volkoh.de/vokoscreen/vokoscreen.html" class="article-link">VokoScreenNG</a>: an open source screencast recording tool used to record all the screen cast demos available in the docs site.

- <a href="(https://shotcut.org/" class="article-link">ShortCut</a>: an open source video editing tool.

### Please find listed below the pull requests (PRs) I opened during GSOD:

1. [Initial Project setup](https://github.com/creativecommons/creativecommons-base/pull/25)
2. <a href="https://github.com/creativecommons/creativecommons-base/pull/28" class="article-link">Adds linter and code formatter</a>
3. <a href="https://github.com/creativecommons/creativecommons-base/pull/30" class="article-link">Adds content for the overview section</a>
4. <a href="https://github.com/creativecommons/creativecommons-base/pull/31" class="article-link">Updates the Overview Section</a>
5. <a href="https://github.com/creativecommons/creativecommons-base/pull/32" class="article-link">Adds the getting started section</a>
6. <a href="https://github.com/creativecommons/creativecommons-base/pull/33" class="article-link">Adds the usage guide section</a>
7. <a href="https://github.com/creativecommons/creativecommons-base/pull/36" class="article-link">Clean Sidebar</a>
8. <a href="https://github.com/creativecommons/creativecommons-base/pull/38" class="article-link">Fix favicon</a>
9. <a href="https://github.com/creativecommons/creativecommons-base/pull/39" class="article-link">Copy to Clipboard</a>
10. <a href="https://github.com/creativecommons/creativecommons-base/pull/40" class="article-link">Fix logo</a>
11. <a href="https://github.com/creativecommons/creativecommons-base/pull/46" class="article-link">Customization content</a>
12. <a href="https://github.com/creativecommons/creativecommons-base/pull/47" class="article-link">Adds copy to the clipboard feature</a>
13. <a href="https://github.com/creativecommons/creativecommons-base/pull/48" class="article-link">Advanced Customizations section</a>
14. <a href="https://github.com/creativecommons/creativecommons-base/pull/49" class="article-link">Updates content for the update theme section</a>
15. <a href="https://github.com/creativecommons/creativecommons-base/pull/50" class="article-link">Adds contributing content</a>
16. <a href="https://github.com/creativecommons/creativecommons-base/pull/52" class="article-link">Fix scroll markdown</a>
17. <a href="https://github.com/creativecommons/creativecommons-base/pull/54" class="article-link">Fixes hamburger in mobile and removes redundant styles</a>
18. <a href="https://github.com/creativecommons/creativecommons-base/pull/55" class="article-link">Removes the static folder its unused</a>
19. <a href="https://github.com/creativecommons/creativecommons-base/pull/56" class="article-link">Updates the site name and homepage content</a>


## CC Base docs - The Outcome

The docs are live 🎉 and are found this url: https://cc-wp-theme-base.netlify.app/

## My lessons

- Working as part of a remotely distributed team I learned a lot about best practices for effective async communication.
- I also learned about etiquette of participating in online meetings: this was especially important skill to learn in 2020 as remote work has since become the norm.
- I was writing prior to gsod but contributing to an org like creative commons in a team with senior developers there was a lot of transfer or knowledge as consequence my writing has immensely improved.
- I learned a new technology: WordPress. This was a challenging feat but I am happy that I persisted and grateful for all the help I got from my team.
