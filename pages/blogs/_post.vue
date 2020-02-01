<template>
  <div>
    <h1>I am blog post {{slug}}</h1>
  </div>
</template>

<script>
export default {
  // async asyncData({ params }) {
  //   this.slug = params.slug // When calling /abc the slug will be "abc"
  //   return { slug }
  // },
  validate({ params }) {
    return /^\d+$/.test(params.post)
  },
  data() {
    return {
      slug: this.$route.params
    }
  },
  created() {
    console.log(this.$route.params)
  },
  mounted() {
    console.log('mounted', this.slug)
  }
}
</script>

<style lang="scss" scoped>
</style>