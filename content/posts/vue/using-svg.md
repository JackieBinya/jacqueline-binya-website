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

[Webp](https://developers.google.com/speed/webp) is a highly perfomant image format create by Google it was created to replace bitmap.

### SVG

![SVG](https://res.cloudinary.com/di70zcupa/image/upload/v1611902092/svg-pic_qexrsj.png)

Scalable Vector Graphics (svg) is a vector image format are created from mathematical formula they don't come bundled with information about how they should be painted that can be computed in the rendering device. SVGs are lighter than bitmap and they are used to create sharp images which scale e.g icons, illustrations etc.

#### The syntax of SVG
- SVG are defined in XML: a markup language.
- The diagram below shows an example of a SVG in raw code:

<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1610570036/svg-sample_k7bupk.png" alt="">

- Lets analyse the definition:

`
💡SVG usually consists of a variety of elements e.g. <path>, </style>,<circle> etc. nested inside an svg element. The inner elements enclosed inside the svg tags are used to describe specific properties of the SVG whereas the outer svg element which is normally referred to as the root element basically instantiate and terminate an instance of SVG.The root element may contain attributes like viewBox,  class, id, fill, height, width and xmlns. The id and class attributes are usually used to extend functionality in Javascript or to style the svg element. The id attribute may also be used in XML specific configurations like the setting up of links. The xmlns attribute is a XML namespace, it is used by the browser to determine how to render the SVG.`

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
- When you project is successfully created🎉, you will get the message below in your terminal:
![Successful vuejs project created](https://res.cloudinary.com/di70zcupa/image/upload/v1611909294/sucesssful-vuejs-install_ddlvl7.png)
The message contains handy scripts to get you started!
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

- I have created a sample SVG to use in the interactive examples provided.. You may go ahead and download it by clicking this 
<a href="/posts/css/svg-sample.svg" download="sample" class="article-link">link</a>. 

You may choose to rename the file, then proceed to add it to the root of the `src` directory, such that the structure of the `src` folder is similar to the one below:

<pre>
.
├── App.vue
├── assets
│   ├── logo.png
│   └── sample.svg
├── components
│   └── HelloWorld.vue
└── main.js
</pre>

#### Inline SVG

![Inline SVG in Vuejs](https://res.cloudinary.com/di70zcupa/image/upload/v1611922129/inline-svg_jlerxx.png)

When using this method you include the `svg` directly in your markup. It's important to mention that when the `svg` is directly embedded in the document or template as in the case of Vuejs ,there is no need to include the `xlmns` attribute.

The pros of using this method are that you can use CSS to style your `svg` and use Javascript to extend its functionality just as you would a normal HTML element.

The main drawback of this method is that if your `svg` is large or when you have a lot of `svg` your template, your template becomes cluttered. In that case it would be better incorporate SVGs as standalone files as it is explained in the next section.

#### External SVG

To embed the SVG in your Vuejs template you use the methods listed below and always ensure that the `xlmns` attribute is included in your root element otherwise none of the methods provided will work!

(i) Embedding an external svg as an image element in a Vuejs template:
![Embedding an external svg as an image element in a Vuejs template](https://res.cloudinary.com/di70zcupa/image/upload/v1611904084/svg-img-implementantion_bhxx8s.png)

_Note you replace the `<file-name>` with the unique name you gave to the image resource you downloaded in this section._

Using this method limits how you can manipulate the `svg` as it really doesn't exist in the document but it is encapsulated in the <img> element. So at most you can only manipulate it as you would a normal image.

The cons of this method include limitations in styling and in functionality of SVGs and in addition to that if you are dealing with a lot of SVGs in your template it becomes rather cumbersome to keep wrapping them in image elements.

(ii) Using `SVG Loaders`
Vuejs uses Webpack as an asset bundler. Webpack uses a loader for each file type it handles. The loaders for the common file types usually come pre-configured whenever you use Vue CLI to bootstrap your project. What that means is that when you import those file types they can be automatically read.But unfortunately `.svg` loaders do not come pre-configured so you have to download them from [npm](https://www.npmjs.com/) then configure them manually.

There are many modules available on npm which are svg vuejs loaders. In this example we will be using the [vue-svg-loader](https://www.npmjs.com/package/vue-svg-loader). The set up instructions are listed in the link provided, for those who have never installed and configured a module in Vuejs follow the instructions below:

_The instructions below are only suited for a project bootstrapped with Vue CLI._

- To install the module type the command below in your terminal:
```
npm i -D vue-svg-loader vue-template-compiler
```
- In the root of you project directory, create a `vue.config.js` file and copy and past the code below:
```
module.exports = {
  chainWebpack: (config) => {
    const svgRule = config.module.rule('svg');
 
    svgRule.uses.clear();
 
    svgRule
      .use('babel-loader')
      .loader('babel-loader')
      .end()
      .use('vue-svg-loader')
      .loader('vue-svg-loader');
  },
};
```
Ensure that you save your changes.

Congrats!!!🎊 

You have successfully installed and configured the setting of the `vue-svg-loader`.

Now, let's proceed to learn how we can use the `vue-svg-loader` module to embed SVG in Vuejs.

![using SVG loaders to embed svg in Vuejs](https://res.cloudinary.com/di70zcupa/image/upload/v1611925461/using-svg-loader_ximunw.png)

- You first remove all the boilerplate code from the `App.vue` file in the `src` directory.
- Then you copy and paste the code above in `App.vue` and save your changes.
- The SGV I used exists as a standalone file in the assets folder as is named `sample.svg`, so depending on what you named your .svg file you may need to tweak the code above.
- Run the below on your terminal, and then on your browser visit ` http://localhost:8080/` to view the Vuejs app with the embedded SVG 🚀.
```
npm run serve
```
The cons of using this method are:
- Your template is kept clean,
- And there are no limitations on how you can style or extend the functionality of your svg.

### References
1. <a href="https://youtu.be/hA7ESX7FsE4" class="article-link">What are Scalable Vector Graphics (SVG) & how are they special? | Web Demystified Episode 4<a>
2. <a href="https://stackoverflow.com/questions/43804171/how-to-extract-svg-as-file-from-web-page/43804258" class="article-link">Stackoverflow Post - How to extract svg as a file from a web page <a>
