<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Set new goals and become more productive and feel good about your accomplishments.
    </p>
  

      <v-parallax
    height="350"
    src="https://artistjameshooper.com/stock-charts.jpg"
  ></v-parallax>
  <app-new-goal @goalAdded="newGoal"></app-new-goal>
  <app-goal-grid :goals="goals"></app-goal-grid>

   <p>
     Create more goals and help get more work done, by using this simple to use Goal Setter.
    </p>



    
  </div>
</template>

<script>
import GoalGrid from './views/GoalGrid.vue';
import NewGoal from './views/NewGoal.vue';

export default {
  data: function() {
    return {
      goals: [
        'Start your goal now!'
      ],
      maxGoals: 15
    }
  },
  methods: {
    newGoal(goal) {
      this.goals.push(goal);
    }
  },
  components: {
    appGoalGrid: GoalGrid,
    appNewGoal: NewGoal
  },
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
