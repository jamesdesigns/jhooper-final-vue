<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
            <label>Goal</label>
            <textarea class="form-control" rows="3" v-model="goal"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
            <label>Goal</label>
            <button @click.prevent="createNew">Add Goal</button>
            </div>
        </form>

    </div>    
</template>
<script>

export default {
    data: function() {
        return {
            goal: ''
        };
    },
    methods: {
        createNew() {
            this.$emit('goalAdded', this.goal);
            this.goal = '';
        }
    }
}
</script>
<style>
</style>