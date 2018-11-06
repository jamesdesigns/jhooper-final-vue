<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Set new goals and become more productive and feel good about your accomplishments.
    </p>

   <p>
     Create more goals and help get more work done, by using this simple to use Goal Setter.
    </p>
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
a {
  color: #42b983;
}
li {
    display: inline-block;
  margin: 0 10px;
  list-style-type: none;
}
.cards {
  display: flex;
  flex-direction: column;
  border: 1px solid #ccc;
  padding: 5%;
  border-radius: 25px;
  margin: 3%;
}
span {
  color: teal;
}
</style>
