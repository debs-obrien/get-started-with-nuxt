<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>

    <section class="sub-section">
      <h3 class="sub-heading">Default Layout</h3>
      <p>You will notice in your layout folder there is a default.vue. This is what we will use to modify our layout. Here you can put things like your header, footer, menu etc. Things that are going to be shared across all pages</p>
      <p>Once you know how your layout is going to be like the only thing you have to think about is where your page content will go. Once you have that clear make sure you add the nuxt tag as this is the tag that nuxt reads so as to know where to add the content rendered by the page. You will see this already in the default.vue so if you modify this vue just make sure you include it in the correct place.</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">More Layouts</h3>
      <p>You can create as many layouts as you want. Generally you won't have that many but perhaps one for your blog if you have one different to your web and also a 404 can sometimes be designed as a different layout.</p>
      <p>Specifying a different layout is really easy. All you have to do is add the following under export default in your page. If you don't add this then the defualt template will be used.</p>
      <pre><code>layout: 'blog'</code></pre>
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
      title: 'Layout Setup',
      subtitle: "Let's get a layout setup so we can really get going"
    }
  }
}
</script>

<style>
</style>
