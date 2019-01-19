<template>
  <div class="title-wrapper">
    <h1 class="title">{{ title }}</h1>
    <h2 class="subtitle">{{ subtitle }}</h2>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    },
    subtitle: {
      type: String,
      default: ''
    }
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.title-wrapper {
  padding: 0 0 20px 0;
  text-align: center;
  .title {
    font-size: 3em;
  }
  .subtitle {
    font-size: 1.5em;
  }
}
</style>
