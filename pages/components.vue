<template>
  <section>
    <Title :title="title" :subtitle="subtitle"/>

    <section class="sub-section">
      <h3 class="sub-heading">Create a component</h3>
      <p>Before we can add a component we must create one. It is normal to use a capital letter to name your components. Let's create a simple Title component.</p>
      <p>As we are woking with single file components all components will have a template tag a script tag and a style tag. You can create these your self or use a template already created. You can even just copy the logo component that comes with the install, duplicate it and modify it.</p>
      <p>What's important to remember when working with templates is that inside the template tag there must be one parent element that encloses all other elemets otherwise your app will break.</p>
    </section>

    <section class="sub-section">
      <h3 class="sub-heading">Add a component</h3>
      <p>There are only 3 things you have to do to add a component so it really is very simple.</p>
      <p>Let's go to the page where you want to add the component. Let's put it in the index page.</p>
      <p>First you need to import the componet so that the page knows it exists</p>
      <pre><code>import Title from '~/components/Title'</code></pre>
      <p>Next we need to export the component in our script tag.</p>
      <pre><code>export default {
      components: {
      Title
      },</code></pre>
      <p>And finally we need to just add this tag to our html. The tag must be the same name as you called it, in this case Title</p>
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
      title: 'Adding Components',
      subtitle: "Let's get some components into your site"
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
