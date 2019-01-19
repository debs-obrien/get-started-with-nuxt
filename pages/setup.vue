<template>
  <section class="container">
    <div>
      <Title :title="title" :subtitle="subtitle"/>

      <section class="sub-section">
        <h3 class="sub-heading">Setup VS Code</h3>
        <p>I recommend you use VS Code for this project and install the 'vue VS Code Extension Pack' which will set you up with everything you need.</p>
        <p>Next open prettier - code/preferences/settings and search for prettier and make sure that it’s setup how you require it</p>
      </section>

      <section class="sub-section">
        <h3 class="sub-heading">Install Nuxt</h3>
        <p>Once we have all this setup we are ready to install nuxt so open a terminal window. Make sure you are creating it in the desired place so cd myproject for example. When you create a nuxt project it will create a folder for you so keep that in mind when running this command</p>
        <pre><code>npx create-nuxt-app project-name</code></pre>
        <p>Once you run the command you will get the following and one by one in the command you need ot answer the questions. Here is what I reccommend just change the name and description to whatever project you are working on.</p>
        <img src="~/assets/images/nuxt-setup.png" alt="setting up nuxt">
        <p>Once everything is setup you will see the following:</p>
        <img src="~/assets/images/nuxt-commands.png" alt="nuxt commands">
      </section>

      <section class="sub-section">
        <h3 class="sub-heading">Open your project</h3>
        <p>Personally I prefer to open the new project in a new window of VS Code rather than cd into the project as then I am in the right workspace from the start and don't have to think about cd into a folder. However if you prefer to not open the project from the start then just cd into the folder like above chaning learn-nuxt-app for what you called your project. Then if you run the dev command you should see your project :)</p>
        <p>You should now get this lovely message from Nuxt telling you where your project is. Use command and click to open the projet or just copy the route and paste it into your browser</p>
        <img src="~/assets/images/nuxt-running.png" alt="nuxt is running">
      </section>
    </div>
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
      title: 'Setup the App',
      subtitle:
        "Lets start at the very beginning. It's a very good place to start"
    }
  }
}
</script>

<style scoped>
img {
  margin: 20px 0;
}
</style>
