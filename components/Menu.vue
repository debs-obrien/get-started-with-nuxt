<template>
  <b-nav vertical>
    <h2>Create a Nuxt app</h2>
    <b-nav-item>
      <nuxt-link to="/">Home</nuxt-link>
    </b-nav-item>
    <b-nav-item active>
      <nuxt-link to="/setup">Setup</nuxt-link>
    </b-nav-item>
    <b-nav-item>
      <nuxt-link to="/folderStructure">Folder Structure</nuxt-link>
    </b-nav-item>
    <b-nav-item>
      <nuxt-link to="/configuration">Configuration Sass</nuxt-link>
    </b-nav-item>
    <b-nav-item disabled>
      <nuxt-link to="/configuration">Configuration wepback</nuxt-link>
    </b-nav-item>
    <b-nav-item disabled>
      <nuxt-link to="/configuration">Create our layout</nuxt-link>
    </b-nav-item>
    <b-nav-item disabled>
      <nuxt-link to="/configuration">Add a Component</nuxt-link>
    </b-nav-item>
    <b-nav-item disabled>
      <nuxt-link to="/configuration">Create Routes</nuxt-link>
    </b-nav-item>
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
