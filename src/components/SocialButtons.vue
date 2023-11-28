<template>
  <div>
    <div class="q-pt-md q-pb-sm">Connect with me via my social media: </div>
    <div class="q-gutter-x-xs">
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
    url: 'https://www.linkedin.com/in/muhammad-rivandra-ie-frontend/',
    color: 'primary'
  },
  {
    icon: 'mdi-instagram',
    url: 'https://www.instagram.com/rivandram/?hl=en',
    color: 'red'
  },
  {
    icon: 'mdi-github',
    url: 'https://github.com/rivandra0',
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
