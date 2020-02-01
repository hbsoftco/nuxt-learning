<template>
  <div>
    <h1>I am blog post {{slug.post}}</h1>
  </div>
</template>

<script>
export default {
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