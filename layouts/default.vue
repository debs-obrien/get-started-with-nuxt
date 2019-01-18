<template>
  <div class="page-wrapper">
    <div class="grid">
      <div class="grid-item">
        <Menu/>
      </div>
      <div class="grid-item">
        <nuxt/>
      </div>
    </div>
  </div>
</template>
<script>
import Menu from '~/components/Menu.vue'

export default {
  components: {
    Menu
  }
}
</script>

<style>
</style>
