<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Search for the most active stock charts and find the best opportunities.<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
  

      <v-parallax
    height="300"
    src="https://artistjameshooper.com/stock-charts.jpg"
  ></v-parallax>

   <p>
      For guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
       <p>
      For guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>

          <v-parallax
    height="300"
    src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
  ></v-parallax>
    
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
