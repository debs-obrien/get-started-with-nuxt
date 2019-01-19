<template>
  <section class="container">
    <Title :title="title" :subtitle="subtitle"/>

    <section class="sub-section">
      <h3 class="sub-heading">eslint Setup</h3>
      <p>In order to easily fix lint errors we will setup a lint fix script in our package.json. Open your package.json and other scripts add the following line.</p>
      <pre><code>"lint:fix": "eslint --fix --ext .js,.vue --ignore-path .gitignore .”</code></pre>
      <p>Then you can run:</p>
      <pre><code>npm run lint:fix</code></pre>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">stylelint Setup</h3>
      <p>First we shall create a .stylelintrc.json file at the root of our project and add the following:</p>
      <pre><code>{
      "processors": ["stylelint-processor-html"],
      "extends": "stylelint-config-standard",
      "plugins": ["stylelint-scss"],
      "rules": {
      //all your rules can go here
      }</code></pre>
      <p>Next we need to install the packages:</p>
      <pre><code>npm i stylelint-scss stylelint-processor-html stylelint-config-standard -D</code></pre>
      <p>Now lets go to our package.json and add the styleint script so that it looks in our scss files but also our vue files</p>
      <pre><code>"stylelint": "stylelint '**/*.vue' '**/*.scss'"</code></pre>
      <p>In order to run the lint tool to see if you have any errors just type</p>
      <pre><code>npm run stylelint</code></pre>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Pre-commit hooks</h3>
      <p>Let's add some pre commit hooks so that all lint errors must be solved before being allowed to add a commit. This is a great way of making sure your code is clean before you commit.</p>
      <p>First let's install Husky</p>
      <pre><code>npm install husky -D</code></pre>
      <p>Next let's go to our package.json and add the following under the scripts (not inside the scripts)</p>
      <pre><code>"husky": {
      "hooks": {
      "pre-commit": "npm run lint && npm run stylelint"
      }
      },</code></pre>
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
