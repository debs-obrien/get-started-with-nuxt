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
          link: '/sassConfiguration',
          text: 'Sass Configuration'
        },
        {
          link: '/webpackConfiguration',
          text: 'wepback Configuration'
        },
        {
          link: '/template',
          text: 'Create our layout'
        },
        {
          link: '/template',
          text: 'Add a Component'
        },
        {
          link: '/template',
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
