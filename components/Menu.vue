<template>
  <header class="header">
    <div :class="{ 'is-active': isOpen }" class="hamburger" @click="toggle()">
      <span class="line"></span>
      <span class="line"></span>
      <span class="line"></span>
    </div>
    <h2 class="title">Create a Nuxt app</h2>
    <div></div>

    <nav v-show="isOpen" class="nav">
      <div class="nav__container">
        <ul v-for="(item, index) in menu" :key="index" class="list-reset">
          <li class="nav-link" @click="toggle()">
            <nuxt-link :to="item.link" exact>{{ item.text }}</nuxt-link>
          </li>
        </ul>
      </div>
    </nav>
  </header>
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
  mounted() {
    // Register an event listener when the Vue component is ready
    window.addEventListener('resize', this.onResize)
  },

  beforeDestroy() {
    // Unregister the event listener before destroying this Vue instance
    window.removeEventListener('resize', this.onResize)
  },
  methods: {
    toggle: function() {
      if (document.documentElement.clientWidth <= 1023) {
        this.isOpen = !this.isOpen
      }
    },
    onResize(event) {
      if (document.documentElement.clientWidth >= 1024) {
        this.isOpen = true
      }
    }
  }
}
</script>

<style scoped lang="scss">
.nav-link {
  font-size: 1.3em;
  margin-bottom: 10px;
}

.hamburger {
  display: none;
}
.title {
  margin: 20px 0;
}

/* For mobile only */
@media only screen and (max-width: 1023px) {
  .header {
    top: 0;
    width: 100%;
    height: 60px;
    z-index: 995;
    padding: 0 15px;
    display: flex;
    position: fixed;
    flex-direction: row;
    background-color: #fff;
    border-bottom: 1px solid #dbdfe1;
    align-items: center;
    justify-content: space-between;
  }
  .nav {
    /* Basic stuff for making the nav fullscreen */
    display: block;
    position: fixed;
    z-index: 995;
    top: 60px;
    left: 0;
    right: 0;
    bottom: 0;
    overflow-y: auto;
    background-color: #fff;
  }

  .nav__container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: calc(100vh - 60px);
    overflow-y: auto;
    -webkit-overflow-scrolling: touch;
    margin-top: 40px;
  }
  .hamburger {
    display: block;
    z-index: 999;
    .line {
      width: 38px;
      height: 3px;
      background-color: $primary;
      display: block;
      margin: 8px auto;
      transition: all 0.3s ease-in-out;
    }
    &.is-active {
      .line:nth-child(1) {
        transform: translateY(13px) rotate(45deg);
      }
      .line:nth-child(2) {
        opacity: 0;
      }
      .line:nth-child(3) {
        transform: translateY(-9px) rotate(-45deg);
      }
    }
    &:hover {
      cursor: pointer;
    }
  }
  .nav-link {
    padding: 5px 0;
  }
  .nav-link,
  .title {
    text-align: center;
  }
} /* end of media query */
</style>
