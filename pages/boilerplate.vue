<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>

    <section class="sub-section">
      <h3 class="sub-heading">Install the boilerplate</h3>
      <p>To make life easier I have created a boilerplate project that has all the configeration setup for you so that you don't need to. This includes vue, nuxt, webpack config, sass config and linters. It is a great way to get a project up and going fast.</p>
      <p>However if you want to know what I have done and how then see the configs below. If you are going to work witht the boilerplate project then you can skip straight to the layout part</p>
      <p>Once you have cloned the boilerplate and ran npm i to install the dependencies you should checkout the folder structure to understand how nuxt works.</p>
      <div class="links">
        <a href target="_blank" class="button--grey">Boilerplate project coming soon</a>
        <nuxt-link to="/folderStructure" class="button--green">Folder Structure</nuxt-link>
      </div>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Setup a custom project</h3>
      <p>If you prefer to setup the project yourself then you can. I have included a full guide to what and how I have done things.</p>
      <div class="links">
        <nuxt-link to="/nuxtSetup" class="button--green">Setup your Project</nuxt-link>
      </div>
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
      title: 'Boilerplate',
      subtitle: 'Use the boilerplate project where it is all set up for you'
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
