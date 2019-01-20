<template>
  <div class="page-wrapper">
    <div class="grid">
      <div class="grid-item">
        <div class="twitter">
          <a hef="https://twitter.com/debs_obrien">
            <img src="~/assets/images/twitter.png" alt="twitter">
          </a>
          <p class="twitter-handler">
            <a hef="https://twitter.com/debs_obrien">debs_obrien</a>
          </p>
        </div>
      </div>
      <div class="grid-item">
        <Menu/>
      </div>
      <div class="grid-item">
        <nuxt/>
      </div>
      <div class="grid-item">
        <div class="github">
          <a hef="https://github.com/debs-obrien">
            <img src="~/assets/images/github.png" alt="github">
          </a>
        </div>
      </div>
    </div>
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

<style lang="scss" scoped>
.twitter {
  img {
    height: 40px;
  }
}
.github {
  img {
    height: 40px;
  }
}
@media only screen and (min-width: 1023px) {
  .twitter {
    position: fixed;
    bottom: 20px;
    transform: rotate(270deg);
  }
  .twitter-handler {
    position: absolute;
    left: 42px;
    bottom: 16px;
  }
  .github {
    position: fixed;
    bottom: 20px;
  }
}
</style>
