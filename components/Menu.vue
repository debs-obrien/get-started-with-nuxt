<template>
  <b-nav vertical>
    <h2>Create a Nuxt app</h2>
    <b-nav-item>
      <nuxt-link to="/">Home</nuxt-link>
    </b-nav-item>
    <b-nav-item active>
      <nuxt-link to="/setup">Setup</nuxt-link>
    </b-nav-item>
    <b-nav-item>Another Link</b-nav-item>
    <b-nav-item disabled>Disabled</b-nav-item>
  </b-nav>
</template>
<script>
export default {}
</script>

<style scoped scss>
.nav-link {
  text-align: left;
}
</style>
