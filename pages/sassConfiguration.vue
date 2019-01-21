<template>
  <section class="container">
    <Title :title="title" :subtitle="subtitle"/>

    <section class="sub-section">
      <h3 class="sub-heading">Install Sass</h3>
      <p>As we are going to work with sass we will need to install node-sass and sass-loader</p>
      <pre><code>npm i node-sass sass-loader</code></pre>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Create the styles Folder</h3>
      <p>First lets create some folders for your images fonts and styles. Create a folder for each one inside the assets folder. You can name this whatever you like, styles or scss etc</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Adding the styles</h3>
      <p>In the scss folder lets create a styles.scss file and a varialbes.scss file and a fonts.scss file.</p>
      <p>Then open the styles.scss file and add the following so that the fonts and variables are included:</p>
      <pre><code>@import 'fonts';<br>@import 'variables';</code></pre>
      <p>Now you can go to your default.vue page in the layouts folder and cut the styles from there into the styles.scss file. I prefer to have all my styles in the styles.scss instead of tring to remember that there are also some styles in the default layout. However if you have a project with many different layouts then maybe having your styles there works best for you.</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Add your styles to the nuxt config</h3>
      <p>Now that we have created a styles.scss file with our styles you will probably see if you have the dev server open that you now have no styles. So lets now tell Nuxt that that file exists. To do this we need to open our nuxt config and add this to the css option. You may need to change this if your route or name of your styles is differnt. Also you can add more than one should you require however I prefer to add this to the styles.scss so I have a better idea of what is loding without having to open the nuxt config but adding the styles here is a good option for adding any vendor styles that you may require</p>
      <pre><code>css: ['~assets/scss/styles.scss'],</code></pre>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Globally include your variables</h3>
      <p>As you may have seen we have created a varialbes folder. This is where we put our variables such as colors etc. We can have separate files that are imported into this this or we can just add all varialbes here. This will depend on the size of your project. Obviously we want these varialbes to be available across all our components and to save us having to write an import inside each component we can gloabally install this file to make it avaialable everywhere. This is extremely useful for cases such as varaibles or mixins.</p>
      <p>To do this we need to install the nuxt style recources loader</p>
      <pre><code>npm i @nuxtjs/style-resources</code></pre>
      <p>Then we need to tell nuxt which file we want to globally make available. Open the nuxt.config.js and add to the modules the following code:</p>
      <pre><code>modules: [
      ['@nuxtjs/style-resources']
      ],
      styleResources: {
      scss: ['~assets/scss/variables.scss'], 
      }</code></pre>
      <p>In order for this to load properly you will need to stop and start your servers again</p>
      <pre><code>npm run dev</code></pre>
      <p>Yes it's true, you are not going to see anything just yet as we haven't added anything to the varialbes file.</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Test it out</h3>
      <p>To test it out lets create a variable for example a primary color. Add this to your varialbes.scss</p>
      <pre><code>$primary: red;</code></pre>
      <p>Now let's add this to our component. We only have one component. The logo. It's ok for testing so let' do it. In the style tag of the Log add the following:</p>
      <pre><code>lang="scss" scoped</code></pre>
      <p>Here we are telling vue to use scss for the styles and to make the styles scoped so they only effect this component. You can choose to have all components as scoped or just some. The choice is yours. You can also have multiple style tags in your component so you can have a mix of scoped and non scoped. You could also have one for scss and another style tag just for css but really why would you want to?</p>
      <p>Now all you have to do is add a style with the color $primary and you should see the color change.</p>
      <pre><code>body {
      background-color: $primary;
      }</code></pre>
      <p>Ok yes your right it's really ugly but it works but yeh maybe you should delete it :)</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Purge your css</h3>
      <p>When you are building a website, chances are that you are using a css framework like Bootstrap, Materializecss, Foundation, etc... But you will only use a small set of the framework and a lot of unused css styles will be included.</p>
      <p>This is where Purgecss comes into play. Purgecss analyzes your content and your css files. Then it matches the selectors used in your files with the one in your content files. It removes unused selectors from your css, resulting in smaller css files</p>
      <pre><code>npm i nuxt-purgecss</code></pre>
      <p>Next add nuxt purgecss to the moudles section in your nuxt.config</p>
      <pre><code> modules: [
      'nuxt-purgecss',
      ],</code></pre>
    </section>
  </section>
</template>

<script>
import Title from '~/components/Title'

export default {
  components: {
    Title
  },
  data() {
    return {
      title: 'Sass Configuration',
      subtitle: 'Lets set the project up so that we can use sass'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
