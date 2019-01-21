<template>
  <section class="container">
    <div>
      <Title :title="title" :subtitle="subtitle"/>

      <section class="sub-section">
        <h3 class="sub-heading">Setup VS Code</h3>
        <p>I recommend you use VS Code for this project and install the 'vue VS Code Extension Pack' by Sarah Drasner which will set you up with everything you need.</p>
        <h4>Extensions Included</h4>
        <ul class="extensions-list">
          <li>
            <span class="highlight">Vetur</span> - Includes support for .vue files, including but not limited to: Syntax-highlighting, Emmet, Linting / Error Checking, Formatting, Auto Completion, Debugging
          </li>
          <li>
            <span class="highlight">Vue Snippets</span> - These are my own snippets to supercharge Vue application development 🚀
          </li>
          <li>
            <span class="highlight">Prettier</span> - Never worry about formatting your code ever again, keep everything consistent with ease. My suggestion is to add "editor.tabCompletion": true, "editor.formatOnSave": true, to your settings file in preferences.
          </li>
          <li>
            <span class="highlight">Formatting toggle</span> This one is a lifesaver! I love Prettier, but there are times I'm submitting PRs to repos with different formatting rules than I have. Rather than having to either shut off Prettier entirely, update my preferences to match theirs, or submit a noisy PR, I can use this extension to toggle formatting with a quickkey and get everything in! I love it.
          </li>
          <li>
            <span class="highlight">Bracket Pair Colorizer</span> - This extension allows matching brackets to be identified with colours. The user can define which characters to match, and which colours to use. Super handy!
          </li>
          <li>
            <span class="highlight">Bookmarks</span> - Adds a bookmark to places you designate in your file, and allows you to quickly jump between them. Super helpful. Type command + opt + K to create a bookmark and command + opt + J to jump between them 🔖
          </li>
          <li>
            <span class="highlight">Jumpy</span> - We lose a lot of time scanning with a mouse, time we can get back by using our keyboard instead. Jumpy provides fast cursor movement by giving you a couple of keys that offer a hook to get to another part of the document.
          </li>
          <li>
            <span class="highlight">NPM Intellisense</span> - a plugin that autocompletes npm modules in import statements
          </li>
          <li>
            <span class="highlight">ES6 Snippets</span> - quickly spin up ES6 JavaScript with only 3 or 4 characters
          </li>
          <li>
            <span class="highlight">Night Owl Theme</span> - Night Owl Syntax highlighting can be a very personal thing, so you might not want to use this, but I worked hard creating a theme you might like. Especially great for your eyes at night, this theme was developed especially with contrast and colorblindness in mind.
          </li>
        </ul>
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
      title: 'VS Code Setup',
      subtitle: "Let's setup our editor so it works best for us"
    }
  }
}
</script>

<style scoped>
img {
  margin: 20px 0;
}
.extensions-list {
  margin-left: 20px;
  list-style-type: disc;
}
</style>
