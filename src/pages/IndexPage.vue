<template>
  <q-page>
    <section class="row justify-start items-start text-center q-pa-xl" style="height:90vh" >
      <div class="col-md-6 col-sm-6 col-xs-11 text-left q-px-lg q-gutter-sm">
        <div class="text-h2">IT'S ME, <br><strong class="text-h1">Andra</strong></div>
        <div class="text-h4">I make fast and light website 🌠</div>
        <div class="text-h6 q-mb-xl"><i>Web Developer 🕸️ & Industrial Engineer 🏭</i></div>
        <MenuListHorizontal/>
      </div>
      <div class="gt-xs col-md-6 col-sm-6 col-xs-11 row">
        <FaceCarousel/>
      </div>
    </section>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import MenuListHorizontal from 'components/MenuListHorizontal.vue'
import FaceCarousel from 'components/FaceCarousel.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    MenuListHorizontal,
    FaceCarousel
  },
  setup () {

  }
})
</script>

<style>

strong{
  background: linear-gradient(to right, rgb(0, 72, 90) , rgb(141, 241, 141));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
