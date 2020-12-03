---
title: "Project Report GSOD-2020 "
date: 2020-12-03T05:28:31+02:00
draft: false
---


> Prepared by Jacqueline Binya on 29 November 2020

During the Google Season of Docs (GSOD) 2020, I contributed to the Creative Commons(CC) Organization's _Usage guide for the WordPress base theme_ project.

Creative Commons Base is a universal WordPress Theme used to build front facing websites for CC. My role as a technical writer was to create community facing documentation for the CC Base theme collaboratively with the engineering team.

This involved creating the content for the docs, creating all illustrative media and also building the site used to host the documentation.

## Planning - Community Bonding phase

During the GSOD - Community Bonding phase I had a meeting with my mentor Hugo Solar in which we strategized on how to effectively build the docs: this included refining and polishing up our objectives for the project and establishing a workflow for doc development.

The outcome of those deliberations were to:
- Create a Google Doc to persist all the draft content which was accessible to all the team members
- Create a tracker document to manage and evaluate our progress.
- I prepared wireframes for the docs site and decided on the features we wanted to include.
- We chose a documentation tool we wanted to use to build the documentation - we chose to use Gridsome which is a static site generator for Vuejs and used the JamDocs theme to scaffold the docs site. Gridsome has plugins which support Markdown, so  the actual content pages of the docs are written in Markdown.
- With regards to the doc development process we decided that the initial stage would be to create draft content in a Google Doc where both my mentors would then review the draft and suggest changes then I would then implement feedback gathered. After the draft content was approved I then would migrate it to the docs site. We also scheduled Google weekly sync meetings as a team, so as to discuss the content. The mentors were readily available to answer questions on various communication channels and promptly gave me the assistance I required.
Onboarding learning about cc commons workflow
Weekly mentor sessions with mentor
Monthly sessions with cc engineering manager
Taking part in all community meetings 
Establishing community channels 

## We Create the Docs - Content Creation

During the content creation phase, the first step involved creating the skeleton of the actual docs site. We created a git branch called _docs_ within the [creative-commons/wp-base-theme](https://github.com/creativecommons/wp-theme-base) repository. All content related to the documentation is persisted in that branch. So,please feel free to contribute. We then used [JamDocs](https://gridsome.org/starters/jamdocs/), a [Gridsome](https://gridsome.org/) theme to quickly scaffold the site. We had to adapt the theme so as to make it meet our own specific needs, this involved overhauling the styles and changing the functionality of some of the features in the theme. After that was completed, we then created a [Google Doc](https://docs.google.com/document/d/1XmIsMTLstbhRRSaNFP538YOXJiS0G5QrN6EzuqJfRy4/edit?usp=sharing) we use for collaboratively writing the draft content for the docs site.

### Tech Stack
As it was mentioned we used [Gridsome](https://gridsome.org/) a static generator for [Vuejs](https://vuejs.org/). We chose Gridsome because:

- We wanted to lower the barrier of entry to contributing:
    - Gridsome/Vuejs community is very active, help is but a click away.
    - The Gridsome official documentation is very resourceful and well maintained.

- Gridsome is highly flexible: The content for the actual documentation is written in [Markdown](https://www.markdownguide.org/getting-started/) but using [@gridsome/vue-remark](https://gridsome.org/plugins/@gridsome/vue-remark), which is a Gridsome plugin, we are able to use javascript in Markdown. We intend to include a copy to the clipboard Vuejs component in the site.

- Time Constraint: This project is a short running project which has to be completed in a 3 month period. Through the use of JamDocs, a Gridsome templating theme as well various plugins it was easy and fast to get started. We were able to add more functionality to the theme with minimal effort.

- Ease of integrating [CC Vocabulary](https://cc-vocabulary.netlify.app/) with Gridsome: it is a requirement that the general aesthetics of all front facing Creative Commons applications is derived from the CC Vocabulary Design System. Major cons for using a design system include ensuring uniformity in design for all front facing CC products.

### Tools Used
- [Figma](https://www.figma.com/):
Figma was used to make assets(banners, logos and illustrations) in the theme. The illustrative media was created with accessibility in mind and all the topography used in the illustrative assets was derived from the CC Vocabulary.

- [VokoScreenNG](https://linuxecke.volkoh.de/vokoscreen/vokoscreen.html): an open source screencast recording tool used to record all the screen cast demos available in the docs site.

- [ShortCut](https://shotcut.org/): an open source video editing tool.

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

- Working as part of a remotely distributed team I learned a lot about best practices for effective async communication. I learned the importance of expressing myself yourself clearly in writing
- I also learned about etiquette of participating in online meetings 
- I was writing prior to gsod but contributing to an org like creative commons with way more senior developers there was a lot of transfer or knowledge as consequence my writing has immensely improved.
- I learned a new technology: WordPress. This was a challenging feat but I am happy I persisted and grateful for all the help I got from my team.
