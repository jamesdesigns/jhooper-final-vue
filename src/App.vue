<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/layout">Layout</router-link> |
      <router-link to="/test">Test</router-link> |
      <router-link to="/login">Login</router-link>
    </div>

    <!-- NEW -->
    <div id="app" class="container">
      <goal-list></goal-list>
    </div>
    <router-view/>


  </div>
</template>

<script>
// New
import HelloWorld from './components/HelloWorld'
// NEW
import GoalList from './components/GoalList'

 export default {
    // NEW
    name: 'App',
    // NEW
    components: {
      HelloWorld,
      GoalList,
    },

    data: () => ({ 
      links: [
        'Home',
        'About Us',
        'Layout',
        'Test'
      ]
    })
  }
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

/* NEW */
* {
  box-sizing: border-box;
}
/* NEW */
.container {
  max-width: 600px;
  margin: 0 auto;
}
</style>
