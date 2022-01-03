<template>
  <div >
      <h1>404</h1>
      <h2>Page not found</h2>
      <button @click="goBack()" class="btn-nav">Go Back</button>
  </div>
</template>

<script>
export default {
  methods: {
    goBack() {
      // this.$router.push({ name: 'Home'})
      this.$router.go(-1)
    }
  }
}
</script>

<style>

</style>