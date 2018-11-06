<template>
  <div class="container">
      <div class="row">
          
              <h1>Animations</h1>
              <hr>
              
              <button @click="show = !show">Show Alert</button>
              <br><br>
              
              <v-card>
              <transition name="fade">
              <div class="" v-if="show">This is some Info</div>
              </transition>
              </v-card>
              <v-card>
              <transition name="slide" type="animation">
              <div class="" v-if="show">This is some Info</div>
              </transition>
              </v-card>
              <v-card>
              <transition 
              appear
              enter-active-class="animated bounce"
              leave-active-class="animated shake"
              >
              <div class="" v-if="show">This is some Info</div>
              </transition>
              </v-card>

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
.fade-enter {
    opacity: 0;
}

.fade-enter-active {
    transition: opacity 1s;
}

.fade-leave {
    /*opacity: 1;*/
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
