<template>
 <!-- <div class="about">
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
  </div> -->
<v-container grid-list-xl>
  <v-layout row wrap>
    <v-flex v-for="ship in starships" :key="ship.model" xs4>
      <v-card
      height="225px">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">{{ ship.name }}</h3>
            <div>{{ ship.model }}</div>
            <span>{{ ship.manufacturer }}</span>
           </div>  
        </v-card-title>



        <v-card-action>
          <v-btn flat color="blue">Search</v-btn>
          </v-card-action>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>

</template>
<script>
import { films } from '../assets/films'
import { starships } from '../assets/starships'
import { planets } from '../assets/planets'

export default {
  data: function() {
    return {
      allFilms: films,
      starships,
      planets
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
span {
  color: teal;
}

</style>