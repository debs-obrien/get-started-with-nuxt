<template>
  <section class="container">
    <Title :title="title" :subtitle="subtitle"/>
    <section class="sub-section">
      <h3 class="sub-heading">Routes</h3>
      <p>Nuxt includes vue router by default so there really isn't much you have to do. In fact everything that goes inside your pages folder will be automatically created as a route and code splitted too.</p>
      <p>So what do you have to do?</p>
      <p>The only thing you have to do is add the nuxt-link tag to what you want to link to with a
        <span class="highlight">:to="/"</span> to go to the home page or
        <span class="highlight">:to="about"</span> to go to the about page.
      </p>
      <p>By default nuxt adds an active class when you are on the correct route so you can just style the active class in your html.</p>
      <p>
        For the home route you will need to put the word
        <span class="highlight">"exact"</span>
        so as the active class will be the exact route for the home and not just every route that contains a slash
      </p>
      <pre class="source-component-vue"><code>
        <span>&#60;nuxt-link :to="/" exact &#62;Home&#60;&#47;nuxt-link&#62;</span>
        <span>&#60;nuxt-link :to="/about"&#62;About&#60;&#47;nuxt-link&#62;</span>
      </code></pre>
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
      title: 'Routes',
      subtitle: "Let's create some routes"
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
