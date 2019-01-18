<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>
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
      title: 'webpack Configuration',
      subtitle: 'Lets get webpack configured'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
