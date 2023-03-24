<template>
  <q-carousel
    swipeable
    animated
    v-model="slide"
    :autoplay="2500"
    ref="carousel"
    infinite
    class="col self-end"
    style="max-width: 500px; min-height: 500px;"
  >
    <q-carousel-slide :name="1" img-src="./assets/faces/01_messy_hair.png" >
      <!-- <div class="relative-position full-height">
        <q-tooltip class="bg-indigo text-md" :offset="[5, 5]">
          SWIPE
        </q-tooltip>
      </div> -->
    </q-carousel-slide>
    <q-carousel-slide :name="2" img-src="./assets/faces/02_jack-Sparrow.png" />
    <q-carousel-slide :name="3" img-src="./assets/faces/03_codet.png" />
    <q-carousel-slide :name="4" img-src="./assets/faces/04_naruto.png" />
    <q-carousel-slide :name="5" img-src="./assets/faces/05_bald.png" />
  </q-carousel>
</template>

<script>
import { ref } from 'vue'
export default {
  // name: 'ComponentName',
  setup () {
    return {
      slide: ref(1)
      // autoplay: ref(true)
    }
  }
}
</script>
