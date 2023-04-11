<template>
    <div class="col-12 parent row justify-center">
      <q-carousel
        swipeable
        animated
        v-model="slide"
        :autoplay="2500"
        ref="carousel"
        infinite
        class="col-12"
        :style="`max-width: ${maxWidth}; min-height: ${minHeight};`"
      >
        <q-carousel-slide :name="1" img-src="../assets/faces/01_messy_hair.png" ></q-carousel-slide>
        <q-carousel-slide :name="2" img-src="../assets/faces/02_jack-Sparrow.png" />
        <q-carousel-slide :name="3" img-src="../assets/faces/03_codet.png" />
        <q-carousel-slide :name="4" img-src="../assets/faces/04_naruto.png" />
        <q-carousel-slide :name="5" img-src="../assets/faces/05_bald.png" />
      </q-carousel>
      <q-img
        src="logos\vue-js-icon.png"
        class="hanging-icon hanging-left-bottom"
        :width="iconSize"
      >
        <q-tooltip :offset="[10, 10]">Quasar Js</q-tooltip>
      </q-img>
      <q-img
        src="logos\quasar-logo-vertical.svg"
        class="hanging-icon hanging-right-top"
        :width="iconSize"
      >
        <q-tooltip :offset="[10, 10]">Quasar Js</q-tooltip>
      </q-img>
      <q-img
        src="logos\pinia-logo.svg"
        class="hanging-icon hanging-right-bottom"
        :width="iconSize"
      >
      <q-tooltip :offset="[10, 10]">Pinia</q-tooltip>
      </q-img>
    </div>
</template>

<script>
import { ref } from 'vue'
export default {
  // name: 'ComponentName',
  props: {
    maxWidth: String,
    minHeight: String,
    iconSize: String
  },
  setup () {
    return {
      slide: ref(1)
      // autoplay: ref(true)
    }
  }
}
</script>

<style>
@keyframes bouncing {
  0%   {transform:translate(0, 0)}
  50% {transform:translate(0, -30px)}
  100% {transform:translate(0, -0)}
}

.hanging-icon{
  position: absolute;
  filter: drop-shadow(0 10px 10px rgba(0, 0, 0, 0.4));
  animation-name: bouncing;
  animation-duration: 2s;
  animation-delay: 1s;
  animation-iteration-count: infinite;
}
.hanging-left-bottom{
  right: 70%;
  top: 50%;
}

.hanging-right-top{
  right: 25%;
  top: 10%;
}

.hanging-right-bottom{
  right: 25%;
  top: 65%;
}

.parent {
  position: relative;
}

</style>
