<template>
  <section class="container">
    <div>
      <Title :title="title" :subtitle="subtitle"/>

      <section class="sub-section">
        <h3 class="sub-heading">Setup VS Code</h3>
        <p>I recommend you use VS Code for this project and install the 'vue VS Code Extension Pack' which will set you up with everything you need.</p>
        <p>Next open prettier - code/preferences/settings and search for prettier and make sure that it’s setup how you require it</p>
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
</style>
