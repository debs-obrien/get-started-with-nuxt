<template>
  <section class="container">
    <div>
      <h1 class="title text-center">Folder Structure</h1>
      <h2 class="subtitle text-center">Lets walk through how the folders are structured.</h2>
      <p>Open your project in vs code and you should see the following if you have follwed the instructions in setup:</p>
      <img src="~/assets/images/folder-structure.png" alt="nuxt folder structure">
      <ul>
        <li>
          <span class="emphasize">nuxt:</span> This is where all the magic works and where you will find your dist folder when you use the build commands. You don't and shouldn't have to change anything in here
        </li>
        <li>
          <span class="emphasize">assets:</span> This is where your assets should go for example sass files, fonts etc
        </li>
        <li>components: This is where we will put all our amazing components that we are going to build</li>
        <li>
          <span class="emphasize">layouts:</span> This folder contains your layouts. You possibly only need one which is default.vue but you may want more for example if you blog had a different layout to the rest of your site then you could create that here and then in the blog file you would add layout: 'blog' to the export default. You could also create a different layout for the error page. I normally just modify the default layout to suit my needs but you may want to create a custom one and leave the default as it is. The choice is yours. For more info on layouts see the
          <a
            href="https://nuxtjs.org/guide/views#layouts"
          >Nuxt docs</a>
        </li>
        <li>
          <span class="emphasize">middleware</span>This directory contains your application middleware. We won't be using this folder in this project. You can delete it or leave it there incase things change in the future.
        </li>
        <li>
          <span class="emphasize">node_modules:</span>Where all your npm packages live
        </li>
        <li>
          <span class="emphasize">pages:</span>This is where all the pages of your site will go from index to about to contact etc
        </li>
        <li>
          <span class="emphasize">plugins:</span>This directory contains your Javascript plugins that you want to run before mounting the root Vue.js application.
        </li>
        <li>
          <span class="emphasize">static:</span>This directory contains your static files.
          Each file inside this directory is mapped to `/`. Robots, favicon etc can go in here.
        </li>
        <li>
          <span class="emphasize">store:</span>This is where vuex store is for all data we want to put in the store. Creating a file in this directory activates the option in the framework automatically.
        </li>
        <li>
          <span class="emphasize">.editorconfig:</span>This is the rules for our editior for spacings and tailing whitespaces etc
        </li>
        <li>
          <span class="emphasize">eslintrc.js:</span>This is where our eslint config lives to define what is considered a lint error. You can modify and add to if if you require
        </li>
        <li>
          <span class="emphasize">.gitignore:</span>This is where you put anything that you want to be ignored in git. This has already been completed for you so you just need to add to it if there is anything extra that you don't want git to know about.
        </li>
        <li>
          <span class="emphasize">.prettierrc:</span>Here is where you have your options for prettier to keep your code pretty. You can modify this if you need to.
        </li>
        <li>
          <span class="emphasize">nuxt.config:</span>Probably the most important file of the project. Here is where you sill configure everthing you need for nuxt. We will do that very soon but to give you an idea it contains webpack config, headers of your page, modules, plugins etc
        </li>
        <li>
          <span class="emphasize">package-lock.json:</span>This is created automatically and makes sure your versions are sthe same across users. You don't need to modify this at all
        </li>
        <li>
          <span class="emphasize">package.json:</span>This is also one of the most important parts of your project as this lets anyone know what your project has and what it can do. It contains things like your scripts and your dependencies.
        </li>
        <li>
          <span class="emphasize">README.md:</span>This is your readme. As the name suggests you should read it. This contains valuable info on how to run your project. This can be added to as you create new scripts etc
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  components: {}
}
</script>

<style scoped scss>
.emphasize {
  color: green;
  font-weight: bold;
}
</style>
