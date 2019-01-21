<template>
  <section class="container">
    <Title :title="title" :subtitle="subtitle"/>
    <section class="sub-section">
      <h3 class="sub-heading">webpack Analyzer</h3>
      <p>Nuxt.js use webpack-bundle-analyzer to let you visualize your bundles and how to optimize them. This is all setup for you so the only thing you have to do is run it.</p>
      <p>You can create a script in your package.json</p>
      <pre class="source-package-json"><code>
        <span>"analyze": "nuxt build -a"</span>
      </code></pre>
      <p>Or you can just type:</p>
      <pre class="source-terminal"><code>
        <span>npm run build -- -a</span>
      </code></pre>
      <p>The analyzer will open a separate window for you to analyze your code</p>
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
