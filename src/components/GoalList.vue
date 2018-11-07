<template>
<div>
    <input type="text" class="goal-input" placeholder="Create your new goal..." v-model="newGoal">
  <div v-for="goal in goals" :key="goal.id" class="goal-item">
      {{ goal.title }}
      </div>
    </div>
</template>

<script>
export default {
  name: 'goal-list',
  data() {
      return {
          newGoal: '',
          goals: [
              {
                  'id': 1,
                  'title': 'Finish Vue Project',
                  'completed': false,
              },
                {
                  'id': 2,
                  'title': 'Code 100 days in a row',
                  'completed': false,
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
input {
    width: 50%;
    border: 1px solid #cccccc;
    padding: 15px 25px;
    font-size: 40px;
    margin-bottom: 16px;
}
.goal-item {
    text-align: left;
}
</style>
