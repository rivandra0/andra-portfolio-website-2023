<template>
  <q-page padding>
    <section class="row justify-start text-left q-px-xl q-pb-xl" style="height:85vh">
      <div class="col-12 row text-h2">
        Skill Set
      </div>
      <div class="col-12 row">
        <q-list class="col-md-4 col-sm-4 col-xs-10 q-my-md">
          <div class="text-h6"><strong>Web Development</strong></div>
          <q-item v-for="logo in logos" :key="logo.name" clickable v-ripple >
            <q-item-section avatar>
              <q-img
                :src="logo.url"
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

const logos = [
  {
    name: 'Vue JS (FE)',
    url: '../assets/logos/vue-js-icon.png'
  },
  {
    name: 'Quasar JS (FE)',
    url: '../assets/logos/quasar-logo-vertical.svg'
  },
  {
    name: 'Express JS (BE) *Just a little',
    url: '../assets/logos/express-js-icon.png'
  },
  {
    name: 'Prisma (ORM)',
    url: '../assets/logos/icons8-prisma-orm-50.png'
  },
  {
    name: 'Wordpress (CMS)',
    url: '../assets/logos/wordpress-icon.png'
  }
]

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
  'Optimizing things ...',
  'Basically the skills every Industrial Engineer should Have'
]

export default {
  // name: 'PageName',
  setup () {
    return {
      logos,
      ITStuff,
      IE
    }
  }
}
</script>
