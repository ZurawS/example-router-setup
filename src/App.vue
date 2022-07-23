<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'about' }">About</router-link> |
    <router-link :to="{ name: 'jobs' }">Jobs</router-link>
  </nav>

  <div>
    <button @click="redirect">Redirect</button>
    <button @click="back">Go back</button>
    <button @click="forward">Go forward</button>
  </div>

  <router-view />
</template>

<script>
export default {
  methods: {
    redirect() {
      this.$router.push({ name: "home" });
    },
    back() {
      this.$router.go(-1);
    },
    forward() {
      this.$router.go(1);
    },
  },
};
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
  color: #2c3e50;
  text-decoration: none;
}

nav a.router-link-exact-active {
  padding: 8px 12px;
  border-radius: 20px;
  background: #42b983;
  color: #fff;
}

.page-content {
  padding: 20px;
  border-radius: 40px;
  margin: 0 20%;
  background: #ddd;
}

.page-content p {
  text-align: left;
}

button {
  padding: 10px;
  margin: 0 10px 10px;
  border: none;
  border-radius: 44px;
  background: #42b983;
  color: #fff;
  cursor: pointer;
}
</style>
