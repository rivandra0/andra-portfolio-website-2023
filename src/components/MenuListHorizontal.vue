<template>
  <router-link class="my-link" v-for="menu in menus" :key="menu.label" :to="menu.target" >
    <q-btn size="md" color="white" text-color="green-9" :label="menu.label" class="q-mr-sm q-mb-sm" push>
      <q-tooltip class="bg-white" :offset="[10,10]">
        <div class="text-h5">{{menu.message}}</div>
      </q-tooltip>
    </q-btn>
  </router-link>
</template>

<script>

const menus = [
  {
    label: 'About',
    target: '/about',
    message: '👨'
  },
  {
    label: 'Skillset',
    target: '/skillset',
    message: '🔧'
  },
  {
    label: 'Projects',
    target: '/projects',
    message: '🚧'
  },
  {
    label: 'Contact',
    target: '/contact',
    message: '🤙'
  }
]

export default {
  name: 'MenuListHorizontal',
  setup () {
    return {
      menus
    }
  }
}
</script>

<style>
.my-link{
  text-decoration: none
}

</style>
