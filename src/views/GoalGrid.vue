<template>
    <div class="row">
        <app-goal v-for="goal in goals">{{ goal }}</app-goal>
    </div>    
</template>
<script>
import Goal from './Goal.vue';
export default {
    props: ['goals'],
    components: {
        appGoal: Goal
    }
}
</script>
<style>
</style>