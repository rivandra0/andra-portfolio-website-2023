<template>
  <q-page>
    <HeroHead/>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import HeroHead from 'src/components/HeroHead.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    HeroHead
  },
  setup () {
    // const pixiContainer = ref(null)
    // const app = null

  }
})
</script>
