<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>
    <section class="sub-section">
      <h3 class="sub-heading">--</h3>
      <p>.....</p>
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
      title: 'page coming soon',
      subtitle: ''
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
