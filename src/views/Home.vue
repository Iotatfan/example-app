<template>
  <div class="home">
    <div>
      <img alt="Vue logo" src="../assets/logo.png">
    </div>
    <h1>Welcome</h1>
    <button @click="userPage('lebah_ganteng')" class="btn-nav">Lebah Ganteng</button>
    <button @click="userPage('kucing_lucu')" class="btn-nav">Kucing Lucu</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  methods: {
    userPage(username = "default_user") {
      this.$router.push({ name: 'User', params: { username: username}})
    }
  }
}
</script>
