<template>
  <nav>
    <router-link :to="{ name: 'home' }">Home</router-link> 
    <router-link :to="{ name: 'about' }">About</router-link>
    <router-link :to="{ name: 'job' }">Job List</router-link>
  </nav>

  <button @click="redirectPage">Redirect</button>
  <button @click="goBack">Back</button>
  <button @click="goForward">Forward</button>
  <router-view/>
</template>

<script>
export default {
  methods: {
    goBack() {
      this.$router.go(-1)
    },
    goForward() {
      this.$router.go(1)
    },
    redirectPage() {
      this.$router.push({ name: 'home'})
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: white;
  background: grey;
  padding: 0.5rem 1rem;
  text-decoration: none;
  margin: 2rem;
  border-radius: 10px;
}

nav a.router-link-exact-active {
  color: white;
  background: blue;
}

button {
  background: rgb(88, 128, 30);
  color: white;
  font-weight: bold;
  margin: 5 rem;
  padding: 0.5rem;
}
</style>
