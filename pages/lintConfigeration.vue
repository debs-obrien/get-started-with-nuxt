<template>
  <section class="container">
    <Title :title="title" :subtitle="subtitle"/>

    <section class="sub-section">
      <h3 class="sub-heading">eslint Setup</h3>
      <p>In order to easily fix lint errors we will setup a lint fix script in our package.json. Open your package.json and other scripts add the following line.</p>
      <pre class="source-terminal"><code>
        <span>"lint:fix": "eslint --fix --ext .js,.vue --ignore-path .gitignore ."</span>
      </code></pre>
      <p>Then you can run:</p>
      <pre class="source-terminal"><code>
        <span>npm run lint:fix</span>
      </code></pre>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">stylelint Setup</h3>
      <p>First we shall create a .stylelintrc.json file at the root of our project and add the following:</p>
      <pre class="source-style-lint"><code>
        <span>{</span>
          <span>"processors": ["stylelint-processor-html"],</span>
          <span>"extends": "stylelint-config-standard",</span>
          <span>"plugins": ["stylelint-scss"],</span>
          <span>"rules": {</span>
            <span>//all your rules can go here</span>
        <span>}</span>
      </code></pre>
      <p>Next we need to install the packages:</p>
      <pre class="source-terminal"><code>
        <span>npm i stylelint-scss stylelint-processor-html stylelint-config-standard -D</span>
      </code></pre>
      <p>Now lets go to our package.json and add the styleint script so that it looks in our scss files but also our vue files</p>
      <pre class="source-nuxt-config"><code>
        <span>"stylelint": "stylelint '**/*.vue' '**/*.scss'"</span>
      </code></pre>
      <p>In order to run the lint tool to see if you have any errors just type</p>
      <pre class="source-terminal"><code>
        <span>npm run stylelint</span>
      </code></pre>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Pre-commit hooks</h3>
      <p>Let's add some pre commit hooks so that all lint errors must be solved before being allowed to add a commit. This is a great way of making sure your code is clean before you commit.</p>
      <p>First let's install Husky</p>
      <pre class="source-terminal"><code>
        <span>npm install husky -D</span>
      </code></pre>
      <p>Next let's go to our package.json and add the following under the scripts (not inside the scripts)</p>
      <pre class="source-package-json"><code>
        <span>"husky": {</span>
          <span>"hooks": {</span>
            <span>"pre-commit": "npm run lint && npm run stylelint"</span>
          <span>}</span>
        <span>},</span>
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
      title: 'Lint Configuration',
      subtitle: 'Lets add some linters for cleaner code'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
