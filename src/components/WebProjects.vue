<template>
  <q-list bordered>
    <q-item v-for="project in projects" :key="project.name" class="column q-gutter-md q-mb-xl" >
      <div class="row justify-center q-gutter-md" >
        <q-item-section class="col-12 row justify-center" style="width:400px">
          <q-img
            :src="project.pictureUrl"
            :ratio="16/9"
            spinner-color="primary"
            spinner-size="82px"
            img-class="my-img"
          />
        </q-item-section>
        <div class="col-12">
          <q-item-section class="text-h6 text-bold">{{project.name}}</q-item-section>
          <q-item-section class="text-p">{{project.description}}</q-item-section>
        </div>
      </div>
      <div class="row justify-end">
          <q-btn-group push>
            <q-btn target="_blank" icon="mdi-file-document-outline" label="Docs" :disable="project.docs === null" :href="project.docs"/>
            <q-btn target="_blank" icon="mdi-github" label="Github" :disable="project.github === null" :href="project.github"/>
            <q-btn target="_blank" icon="mdi-arrow-right" color="green-7" label="Visit site" :disable="project.siteUrl === null" :href="project.siteUrl" />
          </q-btn-group>
      </div>
    </q-item>
  </q-list>
</template>

<script>
const projects = [
  {
    name: 'Collectoria',
    description: 'Simple app to collect time data from multiple objects',
    pictureUrl: '/project/collectoria.jpeg',
    github: 'https://github.com/TuyulMohak/collectoria-frontend.git',
    docs: null,
    siteUrl: null
  },
  {
    name: 'My Old Portfolio Website',
    description: 'This is my first portfolio website made using Quasar js',
    pictureUrl: '/project/old-portfolio-website.jpeg',
    github: 'https://github.com/TuyulMohak/first-portfolio-web.git',
    docs: null,
    siteUrl: 'https://andra-site.netlify.app/#/'
  },
  {
    name: 'Andranote',
    description: 'Simple note app, made using Quasar js, Express js and Prisma ORM, and published on Netlify and Glitch',
    pictureUrl: '/project/andranote.jpeg',
    github: 'https://github.com/TuyulMohak/andranote-frontend.git',
    docs: null,
    siteUrl: 'https://andranote.netlify.app/#/'
  },
  {
    name: 'PT Geotex Prima Profil Website (Wordpress)',
    description: 'Profile website for a company',
    pictureUrl: '/project/geotexprima.png',
    github: null,
    docs: null,
    siteUrl: null
  },
  {
    name: 'Rendang Adventure',
    description: 'A simple platformer game made for mobile. made using Godot engine',
    pictureUrl: '/project/Rendang Adventure.webp',
    github: null,
    docs: null,
    siteUrl: 'https://tuyulmohak1.wordpress.com/2022/01/21/first-publish/'
  }
]

export default {
  // name: 'ComponentName',
  setup () {
    return {
      projects
    }
  }
}
</script>

<style>
.my-img{
  border: 2px solid #555
}
</style>
