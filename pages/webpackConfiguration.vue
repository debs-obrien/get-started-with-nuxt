<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>
    <section class="sub-section">
      <h3 class="sub-heading">webpack Analyzer</h3>
      <p>Nuxt.js use webpack-bundle-analyzer to let you visualize your bundles and how to optimize them.</p>
      <p>Go to your nuxt-config and add the following</p>
      <pre><code>build: {
      analyze: true,
      }</code></pre>
      <p>Then run the analyzer and get analyzing</p>
      <pre><code>nuxt build -a</code></pre>
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
