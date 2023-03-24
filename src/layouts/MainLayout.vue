<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-transparent">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          size="xl"
          color="black"
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title class="text-black">
          Muhammad Rivandra
        </q-toolbar-title>

        <!-- <div>Quasar v{{ $q.version }}</div> -->
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered

    >
      <q-list class="q-pa-md">
        <q-item v-for="menu in menus" :key="menu.label" :to="menu.target" class="text-h4 text-left" active-class="active" clickable ripple exact>
          <q-item-section>
            <q-item-label >{{menu.label}}</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

const menus = [
  {
    label: 'Home',
    target: '/',
    message: ''
  },
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

export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      menus,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>

<style>
body{
  font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif ;
}
.active{
  color: rgb(0, 139, 19);
  text-decoration: underline;
}
</style>
