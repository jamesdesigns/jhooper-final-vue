<template>
  <div class="about">
    <div class="cards">
    <h1>Star Wars Films</h1>
    <ul id="example-1">
      <li v-for="film in allFilms" :key="film.episode_id">
        {{ film.title }}
        </li>
      </ul>
    </div> 
    <div class="cards">
      <h1>Top Starships</h1>
      <ul id="example-1">
        <li v-for="shipNames in starships" :key="shipNames.name">
        {{ shipNames.name }}
      </li>
      </ul> 
      </div>
  </div>
</template>
<script>
import { films } from "../assets/films";
import { starships } from '../assets/starships'

export default {
  data: function() {
    return {
      allFilms: films,
      starships
    }
  }
}
</script>
<style>
li {
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

</style>