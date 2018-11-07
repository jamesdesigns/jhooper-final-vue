<template>
  <div class="container">
      <div class="row">
          
              <h1>Summary of Goals</h1>
              
              
              <button @click="show = !show">Show Goals</button>
              <br><br>
              
              
              <transition name="fade">
              <div class="box" v-if="show">Finish the New Vue Project</div>
              </transition>
             
              
              <transition name="slide" type="animation">
              <div class="box" v-if="show">Code for 100 days in a row</div>
              </transition>
              
              
              <transition 
              appear
              enter-active-class="animated fadeIn"
              leave-active-class="animated shake"
              >
              <div class="box" v-if="show">Land a Job with Adobe</div>
              </transition>
          </div>
  </div>
</template>
<script>
  export default {
      data() {
          return {
              show: true
          }
      }
}
</script>
<style>
.box {
    background-color: #cccccc;
    padding: 25px;
    text-align: center;
    margin-bottom: 1%;
}

.fade-enter {
    opacity: 0;
}

.fade-enter-active {
    transition: opacity 1s;
}

.fade-leave {
    opacity: 1;
}

.fade-leave-active {
    transition: opacity 1s;
    opacity: 0;
}

.slide-enter {
    /*transform: translate(20px);*/
    opacity: 0;
}

.slide-enter-active {
    animation: slide-in 1s ease-out forwards;
    transition: opacity .5s;
}

.slide-leave {
    transition: opacity 1s;
}

.slide-leave-active {
    animation: slide-out 1s ease-out forwards;
    transition: opacity 1s;
    opacity: 0;
}

@keyframes slide-in {
    from {
        transform: translate(20px);
    }
    to {
        transform: translate(0);
    }
}

@keyframes slide-out {
    from {
        transform: translate(0);
    }
    to {
        transform: translate(20px);
    }
}
</style>
