<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>
    <section class="sub-section">
      <h3 class="sub-heading">Routes</h3>
      <p>Nuxt includes vue router by default so there really isn't much you have to do. In fact everything that goes inside your pages folder will be automatically created as a route and code splitted too.</p>
      <p>So what do you have to do?</p>
      <p>The only thing you have to do is add the nuxt-link tag to what you want to link to with a :to="/" to go to the home page or :to="about" to go to the about page.</p>
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
