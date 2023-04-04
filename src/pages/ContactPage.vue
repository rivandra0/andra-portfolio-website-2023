<template>
  <q-page padding>
    <section class="row justify-start items-start text-left q-pa-lg">
      <div class="gt-xs col-12 row text-h2 active">Contact</div>
      <div class="lt-sm col-12 row text-h3 active">Contact</div>

      <div class="col-12 row">
        <div class="col-md-6 col-sm-6 col-xs-10 q-py-md">
          <MapJambi/>
        </div>
        <q-list class="col-md-6 col-sm-6 col-xs-10 q-py-md q-ma-none" dense>
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
          <SocialButtons/>
        </q-list>
      </div>

    </section>
  </q-page>
</template>

<script>
import MapJambi from 'components/MapJambi.vue'
import SocialButtons from 'components/SocialButtons.vue'
export default {
  // name: 'PageName',
  components: {
    SocialButtons,
    MapJambi
  }
}
</script>
