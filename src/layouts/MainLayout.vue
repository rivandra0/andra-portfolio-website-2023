<template>
  <q-layout view="lHh Lpr lff">
    <q-header bordered class="q-px-md row items-center bg-white">
      <q-toolbar class="col-12 row items-center">

        <div class="col row item-center">
          <q-item clickable to="/">
            <q-avatar rounded size="35px" font-size="35px" >
              <q-img
                src="icons\android-chrome-192x192.png"
              />
            </q-avatar>
          </q-item>
        </div>
        <div class="col row justify-end">
          <q-btn
            flat
            dense
            round
            color="black"
            icon="menu"
            size="xl"
            aria-label="Menu"
            @click="toggleLeftDrawer"
            class="lt-sm col-4 self-end"
          />
        </div>
        <MenuListHorizontal class="gt-xs"/>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
    >
      <q-list class="q-pa-md text-grey-9">
        <q-item>
          <q-avatar rounded size="35px" font-size="35px" >
            <q-img
              src="icons\android-chrome-192x192.png"
            />
          </q-avatar>
        </q-item>
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

    <q-footer class="text-white text-right row bg-transparent justify-end">
      <div class="absolute-bottom-right bg-green-1 col-md-4 col-sm-6 col-xs-11 text-grey-8" style="border-radius:15px 0 0 0">© 2023 Muhammad Rivandra, All rights reserved.</div>
    </q-footer>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import MenuListHorizontal from 'components/MenuListHorizontal.vue'

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
    MenuListHorizontal
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

</style>
