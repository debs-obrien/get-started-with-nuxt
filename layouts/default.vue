<template>
  <div>
    <b-container fluid>
      <b-row>
        <b-col cols="3">
          <Menu/>
        </b-col>
        <b-col cols="9">
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
