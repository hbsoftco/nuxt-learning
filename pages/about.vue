<template>
  <div>
    <h1>{{title}}</h1>
    <nuxt-link to="/">Home</nuxt-link>
    <n-link to="/">Home</n-link>
    <NuxtLink to="/">Home</NuxtLink>
    <NLink to="/">Home</NLink>
  </div>
</template>

<script>
export default {
  asyncData() {
    return { title: 'About hastam' }
  },
  fetch() {},
  head() {
    return {
      title: 'About',
      script: [
        {
          /*src: '/about.js'*/
        }
      ],
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'My amazing about page'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
</style>