<template>
  <div class="menu">
    <h2>Create a Nuxt app</h2>
    <ul v-for="(item, index) in menu" :key="index">
      <li class="nav-link">
        <nuxt-link :to="item.link">{{ item.text }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      menu: [
        {
          link: '/',
          text: 'Home'
        },
        {
          link: '/setup',
          text: 'Setup'
        },
        {
          link: '/folderStructure',
          text: 'Folder Structure'
        },
        {
          link: '/configurationSass',
          text: 'Sass Configuration'
        },
        {
          link: '/configurationWebpack',
          text: 'wepback Configuration'
        },
        {
          link: '',
          text: 'Create our layout'
        },
        {
          link: '',
          text: 'Add a Component'
        },
        {
          link: '/configuration',
          text: 'Create Routes'
        }
      ]
    }
  }
}
</script>

<style scoped scss>
.nav-link {
  font-size: 1.3em;
  margin-bottom: 10px;
}
</style>
