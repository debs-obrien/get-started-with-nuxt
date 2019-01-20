<template>
  <div>
    <div class="hamburger">
      <button @click="toggle()">Open/Close</button>
    </div>
    <div v-show="isOpen" class="menu">
      <h2>Create a Nuxt app</h2>
      <ul v-for="(item, index) in menu" :key="index">
        <li class="nav-link">
          <nuxt-link :to="item.link">{{ item.text }}</nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isOpen: true,
      menu: [
        {
          link: '/',
          text: 'Home'
        },
        {
          link: '/vsCodeSetup',
          text: 'VS Code Setup'
        },
        {
          link: '/boilerplate',
          text: 'Boilerplate Project'
        },
        {
          link: '/nuxtSetup',
          text: 'Nuxt Setup'
        },
        {
          link: '/sassConfiguration',
          text: 'Sass Configuration'
        },
        {
          link: '/lintConfigeration',
          text: 'Lint Configuration'
        },
        {
          link: '/webpackConfiguration',
          text: 'wepback Configuration'
        },
        {
          link: '/folderStructure',
          text: 'Folder Structure'
        },
        {
          link: '/layoutSetup',
          text: 'Create our layout'
        },
        {
          link: '/components',
          text: 'Add a Component'
        },
        {
          link: '/routes',
          text: 'Create Routes'
        }
      ]
    }
  },
  methods: {
    toggle: function() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style scoped scss>
.nav-link {
  font-size: 1.3em;
  margin-bottom: 10px;
}
.menu {
  display: block;
}
.hamburger {
  display: none;
}
@media only screen and (min-width: 1023px) {
  .menu {
    display: block;
  }
}
@media only screen and (max-width: 1023px) {
  .hamburger {
    display: block;
  }
  .nav-link {
    text-align: center;
  }
}
</style>
