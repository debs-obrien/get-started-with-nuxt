<template>
  <div>
    <b-container fluid>
      <b-row class="text-center">
        <b-col cols="3">
          <Menu/>
        </b-col>
        <b-col>
          <nuxt/>
        </b-col>
      </b-row>
    </b-container>
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
