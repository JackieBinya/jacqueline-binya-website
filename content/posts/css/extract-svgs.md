---
title: "Using SVGs in Vuejs made simple"
date: 2021-01-04T02:19:11+02:00
draft: false
---

## Images of the web

The most commonly used image formats in the web include bitmap, svg and webp.

### Bitmap

Bitmap images are made up from tiny dots called pixels. Each pixel is actually a square which is assigned a specific color and is arranged in a pattern to form the image. When you zoom in on a bitmap you can actually see each pixel. Image formats like JPEG, PNG and GIF are all bitmap. Bitmap format is suited for highly detailed images like photographs.

### Webp

This a highly perfomant image format create by Google.

### SVG

![SVG](https://res.cloudinary.com/di70zcupa/image/upload/v1611902092/svg-pic_qexrsj.png)

Scalable Vector Graphics (svg) is a vector image format are created from mathematical formula they don't come bundled with information about how they should be painted that can be computed in the rendering device. SVGs are lighter than bitmap and they are used to create sharp images which scale e.g icons, illustrations etc.

#### The syntax of SVG
- SVG are defined in XML: a markup language.
- The diagram below shows an example of a SVG in raw code:

<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1610570036/svg-sample_k7bupk.png" alt="">

- Lets analyse the definition:

`
💡SVG usually consists of a variety of elements e.g. <path>, </style>,<circle> etc. nested inside an svg element. The inner elements enclosed inside the svg tags are used to describe specific properties of the SVG whereas the outer svg element which is normally referred to as the root element basically instantiate and terminate an instance of SVG.The root element may contain attributes like viewBox,  class, id, fill, height, width and xmlns. The id and class attributes are usually used to extend functionality in Javascript or to style the svg element. The id attribute may also be used in XML specific configurations like the setting up of links. The xmlns attribute is a XML namespace, it is used by the browser to determine how to render the SVG. Attributes like`

#### Using SVGs in Vuejs

- Generally SVGs can can be incorporated in an HTML document:
    - inline or,
    - as external standalone files.
- The above listed methods can be used in Vuejs.

But before we explore how we can incorporate SVG in a Vuejs web app. First let us create a simple Vuejs application we will use to demonstrate how to embed SVG in Vuejs.

We will be using Vue CLI to bootstrap our project.

Requirements:

- [Nodejs](https://nodejs.org/en/)
- [Vue CLI](https://cli.vuejs.org/)

To create a Vuejs project:
- On your terminal type:
```
vue create <project-name>
```
Replace `<project-name>` with a unique name for your project. My project is name `svg-tutorial`.
- You will then be prompted to pick a preset for your app, just press Enter to choose the default preset which at the time of publishing this article is: `Default ([Vue 2] babel, eslint)`.
- Then wait as Vue CLI creates a Vuejs project for you.
- When you project is successfully created you will get the message below in your terminal:
![Successful vuejs project created](https://res.cloudinary.com/di70zcupa/image/upload/v1611909294/sucesssful-vuejs-install_ddlvl7.png)
The message contains handy command to get you started!
- Let's take a look at our project's file structure paying special attention to the `src` folder since most of our work pertaining to SVG will be restricted to that folder.

<pre>
.
├── babel.config.js
├── node_modules
├── package.json
├── package-lock.json
├── public
├── README.md
└── src
    ├── App.vue
    ├── assets
    │   └── logo.png
    ├── components
    │   └── HelloWorld.vue
    └── main.js
</pre>

- I have created a sample SVG to use in our tutorial. You may go ahead and download it by clicking this 
<a href="/posts/css/svg-sample.svg" download="Using SVG in Vuejs" class="article-link">link</a>.

#### Inline SVG
When using this method you just include the `svg` directly in the template. Its important to mention that when the `svg` is directly embedded in the document or template as in the case of Vuejs there is no need to include the `xlmns` attribute. The main drawback of this method is that when you have a lot of `svg` your template becomes cluttered. In that case it would be better incorporate SVGs as standalone files as it is explained in the next section.
#### External SVG
In this method you include the SVG in your project structure as a standalone `.svg` file. To embed the SVG in your Vuejs template you use the methods listed below:

(i) Embedding an external svg as an image element in a Vuejs template:
![Embedding an external svg as an image element in a Vuejs template](https://res.cloudinary.com/di70zcupa/image/upload/v1611904084/svg-img-implementantion_bhxx8s.png)

(ii) Using `SVG Loaders`
Vuejs uses Webpack as an asset bundler. Webpack uses a loader for each file type it handles. The loaders for the common file types usually come pre-configured in the event you use Vue CLI to bootstrap your project. But unfortunately `.svg` file types are not pre-configured so to read them in your project you have to download specify vue svg loaders.


### References
1. <a href="https://youtu.be/hA7ESX7FsE4" class="article-link">What are Scalable Vector Graphics (SVG) & how are they special? | Web Demystified Episode 4<a>
2. <a href="https://stackoverflow.com/questions/43804171/how-to-extract-svg-as-file-from-web-page/43804258" class="article-link">Stackoverflow Post - How to extract svg as a file from a web page <a>
