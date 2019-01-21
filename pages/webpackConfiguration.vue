<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>
    <section class="sub-section">
      <h3 class="sub-heading">webpack Analyzer</h3>
      <p>Nuxt.js use webpack-bundle-analyzer to let you visualize your bundles and how to optimize them. This is all setup for you so the only thing you have to do is run it.</p>
      <p>You can create a script in your package.json</p>
      <pre><code>"analyze": "nuxt build -a"</code></pre>
      <p>Or you can just type:</p>
      <pre><code>npm run build -- -a</code></pre>
      <p>The analyzer will open a separate window for you to analyze your code</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Extract Css</h3>
      <p>To extract your css into a separate file add the following to your nuxt.config</p>
      <pre><code>build: {
      extractCSS: true,
      }</code></pre>
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
      title: 'webpack Configuration',
      subtitle: 'Lets get webpack configured'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
