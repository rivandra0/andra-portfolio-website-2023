<template>
  <q-page padding>
    <section class="row justify-start text-left q-pa-lg q-gutter-x-xl q-pb-xl">
      <div class="gt-xs col-12 row text-h2 q-mb-xl active">Projects</div>
      <div class="lt-sm col-12 row text-h3 q-mb-xl active">Projects</div>
      <div class="col-md-5 col-sm-10 col-xs-11 ">
        <div class="row text-h5 q-pb-md">
          <strong>Web Development++</strong>
        </div>
        <WebProjects/>
      </div>
      <div class="col-md-4 col-sm-12 col-xs-11 self-right">
        <div class="row text-h5 text-bold q-pb-md q-pt-xl">Graphic Design</div>
        <GraphicDesignCatalog/>
      </div>
    </section>
  </q-page>
</template>

<script>
import WebProjects from 'components/WebProjects.vue'
import GraphicDesignCatalog from 'components/GraphicDesignCatalog.vue'
export default {
  components: {
    WebProjects,
    GraphicDesignCatalog
  }
  // name: 'PageName',
}
</script>
