<template>
  <Title :title="title" :subtitle="subtitle"/>
</template>

<script>
import Title from '~/components/Title'

export default {
  components: {
    Title
  },
  data() {
    return {
      title: 'title',
      subtitle: 'subtitle'
    }
  }
}
</script>

<style>
</style>
