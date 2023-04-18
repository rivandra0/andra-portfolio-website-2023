<template>
  <q-page padding>
    <section class="row justify-start text-left q-pa-lg q-pb-xl">
      <div class="gt-xs col-12 row text-h2 active">Skill Set</div>
      <div class="lt-sm col-12 row text-h3 active">Skill Set</div>
      <div class="col-12 row">
        <q-list class="col-md-4 col-sm-4 col-xs-10 q-my-md">
          <div class="text-h6"><strong>Web Development</strong></div>
          <q-item v-for="logo in logos" :key="logo.name" clickable v-ripple >
            <q-item-section avatar>
              <q-img
                :src="logo.uri"
                spinner-color="primary"
                spinner-size="82px"
              />
            </q-item-section>
            <q-item-section>{{logo.name}}</q-item-section>
          </q-item>
        </q-list>
        <q-list dense class="col-md-4 col-sm-4 col-xs-10 q-my-md">
          <div class="text-h6">Other IT Stuff</div>
          <q-item v-for="stuff in ITStuff" :key="stuff.id" clickable v-ripple >
            <q-item-section>{{stuff}}</q-item-section>
          </q-item>
        </q-list>
        <q-list dense class="col-md-4 col-sm-4 col-xs-10 q-my-md q-mb-xl">
          <div class="text-h6">Industrial Engineering</div>
          <q-item v-for="subject in IE" :key="subject.id" clickable v-ripple >
            <q-item-section>{{subject}}</q-item-section>
          </q-item>
        </q-list>
      </div>

    </section>
  </q-page>
</template>

<script>
// import { ref } from 'vue'
const ITStuff = [
  'Information System Analysis & Design',
  'UI/UX Design',
  'Graphic Design',
  'Web Scraping & Browser Automation',
  'Excel Automation using JS'
]

const IE = [
  'Product Design & Development',
  'Quality Control',
  'Industrial Statistics',
  'System Optimization',
  'Marketing Management',
  'Forecasting'
]

export default {
  // name: 'PageName',
  setup () {
    // const vueLogo = ref('/logos/vue-js-icon.png')
    // const quasarLogo = ref('/logos/quasar-logo-vertical.svg')
    // const expressLogo = ref('/logos/express-js-icon.png')
    // const prismaLogo = ref('/logos/icons8-prisma-orm-50.png')
    // const wordpressLogo = ref('/logos/wordpress-icon.png')
    const logos = [
      {
        name: 'Vue JS (FE)',
        uri: '/logos/vue-js-icon.png'
      },
      {
        name: 'Quasar JS (FE)',
        uri: '/logos/quasar-logo-vertical.svg'
      },
      {
        name: 'Nuxt (FE)',
        uri: '/logos/nuxt.png'
      },
      {
        name: 'Express JS (BE)',
        uri: '/logos/express-js-icon.png'
      },
      {
        name: 'Prisma (ORM)',
        uri: '/logos/icons8-prisma-orm-50.png'
      },
      {
        name: 'Wordpress (CMS)',
        uri: '/logos/wordpress-icon.png'
      }
    ]

    return {
      logos,
      ITStuff,
      IE,
      getLogoPath (fileName) {
        return `/assets/logos/${fileName}`
      },
      getProjectPath (fileName) {
        return `/assets/project/${fileName}`
      }
    }
  }
}
</script>
