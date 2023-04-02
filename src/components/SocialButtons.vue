<template>
  <div class="q-my-xl">
    <div class="q-pa-sm">Or contact me via my social media: </div>
    <div class="q-gutter-x-md">
      <q-btn
        outline
        round
        v-for="data in socialData"
        :key="data.url"
        :icon="data.icon"
        :href="data.url"
        :color="data.color"
        target="_blank"
        size="md"
      />
    </div>
  </div>
</template>

<script>

const socialData = [
  {
    icon: 'mdi-linkedin',
    url: 'https://www.linkedin.com/in/muhammad-rivandra-620277202?originalSubdomain=id',
    color: 'primary'
  },
  {
    icon: 'mdi-instagram',
    url: 'https://www.instagram.com/rivandram/?hl=en',
    color: 'red'
  },
  {
    icon: 'mdi-github',
    url: 'https://github.com/TuyulMohak',
    color: 'black'
  },
  {
    icon: 'mdi-email-outline',
    url: 'mailto:rivandra0@gmail.com',
    color: 'orange'
  }
]

export default {
  setup () {
    return {
      socialData
    }
  }
}
</script>

<style>
a{
  text-decoration: none;
}
</style>
