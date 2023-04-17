<template>
  <q-page padding>
    <section class="row justify-start items-center text-center q-pa-lg q-mb-xl" >
      <div class="lt-sm col-xs-12">
        <FaceCarousel maxWidth="300px" minHeight="300px" iconSize="40px"/>
      </div>
      <div class="col-md-7 col-sm-6 col-xs-12 text-left q-px-md q-gutter-sm">
        <div class="text-subtitle2">It's me, Andra</div>
        <div class="gt-xs text-h2 text-bold text-grey-10">Delivering <strong>Cool</strong> websites with <strong>Vue.js</strong></div>
        <div class="lt-sm text-h4 text-bold text-grey-10">Delivering <strong>Lightning-fast</strong> websites with Vue.js</div>
        <div class="text-subtitle1 text-green-9">Front-end Web Developer, UX Generalist & Industrial Engineer</div>
        <SocialButtons/>
      </div>
      <div class="gt-xs col-5 col-md-5 col-sm-6 col-xs-11 row">
        <FaceCarousel maxWidth="500px" minHeight="500px" iconSize="60px"/>
      </div>
    </section>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import FaceCarousel from 'components/FaceCarousel.vue'
import SocialButtons from 'components/SocialButtons.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    FaceCarousel,
    SocialButtons
  },
  setup () {

  }
})
</script>
