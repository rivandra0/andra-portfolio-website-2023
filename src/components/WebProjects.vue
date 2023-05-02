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
            <q-btn v-if="project.docs !== null" target="_blank" icon="mdi-file-document-outline" label="Docs" :href="project.docs"/>
            <q-btn v-if="project.githubFe !== null" target="_blank" icon="mdi-github" label="FE" :href="project.githubFe"/>
            <q-btn v-if="project.githubBe !== null" target="_blank" icon="mdi-github" label="BE" :href="project.githubBe"/>
            <q-btn v-if="project.siteUrl !== null" target="_blank" icon="mdi-arrow-right" class="text-white" style="background-color: var(--dark-green);" label="Visit site" :href="project.siteUrl"/>
          </q-btn-group>
      </div>
    </q-item>
  </q-list>
</template>

<script>
const projects = [
  {
    name: 'UPTD Logam Disperindag Sumbar',
    description: "I created muaracoder.com to share the latest information on web development and IT, using Nuxt 3 with Tailwind CSS for the design. I implemented Nuxt's SSR and added internalization using the i18n module. Check it out and let me know what you think!",
    pictureUrl: 'Logo_complete_MuaraCoder',
    githubFe: null,
    githubBe: null,
    docs: null,
    siteUrl: 'https://muaracoder.com'
  },
  {
    name: 'UPTD Logam Disperindag Sumbar',
    description: 'I had the opportunity to develop a CMS website using Quasar JS and Supabase for a UPTD Logam Disperindag Sumatera Barat. Throughout the development process, I learned valuable skills such as handling files, routing, and implementing basic authentication. Although the website has yet to be published, I am grateful for the experience and the knowledge I gained in web development. I look forward to applying what I learned in future projects.',
    pictureUrl: 'project/uptd_logam.png',
    githubFe: null,
    githubBe: null,
    docs: null,
    siteUrl: null
  },
  {
    name: 'Dotcom Organization Profile Website',
    description: "I've created a clean and modern profile website for Dotcom, our Student IT organization within the Industrial Engineering department. The site is built entirely using Quasar JS and showcases our organization's mission, members, and projects. With a responsive design and intuitive navigation, it provides a seamless user experience for visitors looking to learn more about our organization. I also designed the new Logo",
    pictureUrl: '/project/dotcom.png',
    githubFe: 'https://github.com/TuyulMohak/dotcom-profile-web.git',
    githubBe: null,
    docs: null,
    siteUrl: 'https://dotcom-hmti-andalas.netlify.app/#/'
  },
  {
    name: 'My New Portfolio Website',
    description: "I'm excited to share my new portfolio website, built with Quasar JS and optimized for responsiveness and performance. With a clean design and intuitive navigation, the site loads quickly and provides a seamless user experience on any device. I'm proud of the site's performance, achieved through techniques such as code minification and image compression, and hope it showcases my skills and projects effectively.",
    pictureUrl: '/project/new-portfolio-website.png',
    githubFe: 'https://github.com/TuyulMohak/andra-portfolio-website-2023',
    githubBe: null,
    docs: null,
    siteUrl: 'https://andra-site.netlify.app/#/'
  },
  {
    name: 'Collectoria',
    description: "I've built a queue data collection tool using Quasar JS, Express, Prisma ORM, and MySQL. The app makes it easy to collect and manage queue data for personal or professional use. With customizable fields and user-friendly features, it provides a simple and efficient solution for queue data management.",
    pictureUrl: '/project/collectoria.jpeg',
    githubFe: 'https://github.com/TuyulMohak/collectoria-frontend.git',
    githubBe: 'https://github.com/TuyulMohak/collectoria-backend.git',
    docs: null,
    siteUrl: null
  },
  {
    name: 'Andranote',
    description: "Andranote is a simple note-taking app that doesn't showcase advanced app creation or design skills. However, it represents an important milestone for me as it was the first app I successfully deployed using various tools and services. I deployed the express backend on Glitch with an external open source MySQL database and used Prisma ORM to handle the database. Additionally, the Quasar JS frontend was deployed on Netlify.",
    pictureUrl: '/project/andranote.jpeg',
    githubFe: 'https://github.com/TuyulMohak/andranote-frontend.git',
    githubBe: null,
    docs: null,
    siteUrl: 'https://andranote.netlify.app/#/'
  },
  {
    name: 'My Old Portfolio Website',
    description: 'My early portfolio website is a simple, single-page site built using Quasar JS. Despite its simplicity, the site features several sections that showcase my skills and projects. While it may not have the bells and whistles of a more advanced website, it serves as a testament to my early efforts in web development and highlights my dedication to learning and improving my skills.',
    pictureUrl: '/project/old-portfolio-website.jpeg',
    githubFe: 'https://github.com/TuyulMohak/first-portfolio-web.git',
    githubBe: null,
    docs: null,
    siteUrl: 'https://andra-site.netlify.app/#/'
  },
  {
    name: 'University Management System Database Design',
    description: 'Made using ERD. The ERD includes entities such as students, courses, faculty, and their respective relationships such as enrollment, advising, and teaching.',
    pictureUrl: '/project/erd-sms.png',
    githubFe: null,
    githubBe: null,
    docs: 'https://drive.google.com/file/d/1hzq82Kqtqb9StF1-i4bXWhKHoj_wPcwt/view?usp=share_link',
    siteUrl: null
  },
  {
    name: 'PT Geotex Prima Profil Website (Wordpress)',
    description: "I built the Geotexprima company profile using Elementor and WordPress. The site showcases the company's construction supply products in a modern and professional design. It's an essential resource for those in the construction industry to easily explore Geotexprima's services and company information.",
    pictureUrl: '/project/geotexprima.png',
    githubFe: null,
    githubBe: null,
    docs: null,
    siteUrl: null
  },
  {
    name: 'Rendang Adventure',
    description: 'A simple platformer game made for mobile. made using Godot engine',
    pictureUrl: '/project/Rendang Adventure.webp',
    githubFe: null,
    githubBe: null,
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
