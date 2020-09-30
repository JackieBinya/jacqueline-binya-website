---
title: "CC WP Base Theme Docs-GSOD-2020: Hello World🚀"
date: 2020-09-29T18:50:55+02:00
tags: ["gsod"]
draft: false
---

> I am participating in the Google Season of Docs 2020 as a technical writer. I am contributing to Creative Commons.

My name is Jacqueline Binya. I am a software developer and technical writer from Zimbabwe. I am going to write a series of blog posts documenting my experience and lessons as I  contribute to the <a class="article-link" href="https://github.com/creativecommons/wp-theme-base"> Creative Commons WordPress Base Theme(CC WP Base Theme) </a> during the <a class="article-link" href="https://developers.google.com/season-of-docs">Google Season of Docs (GSOD-2020) </a> as a technical writer.

## What is Google Season of Docs?

The Google Season of the Docs was born out of a need to improve the quality of open-source documentation as well as to advocate for open source, for documentation, and for technical writing. Annually during the GSOD, technical writers are invited to contribute to open-source projects through a highly intensive process geared at ensuring that the technical writers and the projects they contribute to during GSOD are a good fit, after that has been determined GSOD then resumes.

## Building the docs
The CC WP Base theme is a WordPress theme used to create front-facing Creative Commons (CC) websites. My task is to collaborate with the engineering team to create community facing docs for the theme.

### Guiding principles
The docs should be inclusive meaning: they should be written in an easy-to-understand manner taking care to avoid the use of excessive technical jargon, they should be accessible and they should have support for internationalization. We hope to provide our users with a smooth and memorable experience whilst using the docs hence the docs site should be fast and easy to navigate.

### Technical stack of the project
We decided to build the docs using <a href="https://jamstack.org/" class="article-link">Jamstack</a> to be specific we are using  <a href="https://gridsome.org/" class="article-link">Gridsome</a> a static generator for <a href="https://vuejs.org/" class="article-link">Vuejs</a>. We are using Gridsome as it is highly performant, and it also integrates smoothly with the <a href="https://cc-vocabulary.netlify.app/" class="article-link"> CC Vocabulary </a>. Gridsome also has out-of-the-box support for important features like Google Analytics and <a href="https://www.algolia.com/" class="article-link">Angolia</a>, these features will obviously become useful in future iterations of the docs.To quickly scaffold the docs we used a Gridsome theme called <a href="https://gridsome.org/starters/jamdocs/" class="article-link">JamDocs</a>.

### Progress
Currently, the project is on track. As it's been stated we are creating the docs collaboratively. The very first step in our workflow is to create draft content Google docs. That task is assigned to me. This involves doing lots of research, reading and also testing out the theme. Afterward, my mentors Hugo Solar and Timid Robot Zehta then give me feedback on the draft. Then I implement the feedback and continuously work on improvements. The final step is migrating the approved draft content to the docs projects in markdown format.

### My lessons so far:
- Always ask questions: frankly, the only way you can create good content is when you have a solid understanding of the subject matter.
- It's better to over-communicate than under-communicate especially when working in a remotely - this is especially more important if you encounter blockers whilst executing your work.
- Push that code and open PR quickly and then go ahead and ask for a review don't procrastinate this will ensure  fast turnover you get feedback quickly and can work on improvements.
