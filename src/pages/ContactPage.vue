<template>
  <q-page padding>
    <section class="row justify-start items-start text-left q-pa-xl" style="height:85vh">
      <div class="col-12 text-h1">
        Contact
      </div>
      <q-list class="col-12 q-ma-none" dense>
        <q-item-label class="text-h5">
          Location & E-mail
        </q-item-label>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="positive" name="map" />
          </q-item-section>
          <q-item-section>Jambi City, Indonesia</q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="positive" name="email" />
          </q-item-section>
          <q-item-section>rivandra0@gmail.com</q-item-section>
        </q-item>
      </q-list>
      <SocialButtons/>
    </section>
  </q-page>
</template>

<script>
import SocialButtons from 'components/SocialButtons.vue'
export default {
  // name: 'PageName',
  components: {
    SocialButtons
  }
}
</script>
