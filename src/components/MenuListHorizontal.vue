<template>
  <q-list class="row">
    <q-item clickable class="col" outline v-for="menu in menus" :key="menu.label" :to="menu.target" active-class="active">
      <q-item-section class="text-grey-9 text-h6">{{ menu.label }}</q-item-section>
      <q-tooltip class="bg-white" :offset="[10,10]">
        <div class="text-h5">{{menu.message}}</div>
      </q-tooltip>
    </q-item>
  </q-list>
</template>

<script>

const menus = [
  {
    label: 'Home',
    target: '/home',
    message: '🏠'
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
