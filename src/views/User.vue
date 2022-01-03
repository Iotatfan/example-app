<template>
  <div >
      <h1>{{ $route.params.username }}'s User Page</h1>   
      <div id="nav">
          <router-link :to="{ name: 'Home'}">Home</router-link> | 
          <router-link :to="routeToHello">Hello</router-link> | 
          <router-link :to="{ name: 'Bye', params: { username: $route.params.username}}">Bye</router-link>
      </div>
      <router-view />
  </div>
</template>

<script>
export default {
    computed: {
        routeToHello() {
            return `/user/${this.$route.params.username}/hello`
        },
        // routetoBye() {
        //     return `/user/${this.$route.params.username}/bye`
        // }
    }

}
</script>

<style>

</style>