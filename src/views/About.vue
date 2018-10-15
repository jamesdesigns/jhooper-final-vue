<template>
  <div class="about">
    <h1>{{ created }}This is an about page</h1>
  </div>
</template>
<script>
import { films } from "../assets/films";
export default {
  created: function() {
    console.log(films); // Text goes here
  }
}
</script>
<style>

</style>