<script setup>
import { ref } from 'vue'
import MainLayout from './components/Layout/MainLayout.vue'
import MainNav from './components/Layout/MainNav.vue'
import BasicPage from './components/Page/BasicPage.vue'

let NavItemsArray = ref([
  {
    name: 'Home',
    link: '#',
    target: '_self',
    class: 'nav-link'
  },
  {
    name: 'Services',
    link: '#',
    target: '_self',
    class: 'nav-link'
  },
  {
    name: 'Contact',
    link: '#',
    target: '_self',
    class: 'nav-link'
  }
])
let UserNavItemsArray = ref([
  {
    name: 'Settings',
    link: '#',
    target: '_self'
  },
  {
    name: 'Profile',
    link: '#',
    target: '_self'
  }
])
</script>

<template>
  <main-layout>
    <template v-slot:header>
      <main-nav :navItems="NavItemsArray" :userNavItems="UserNavItemsArray"> </main-nav>
    </template>
    <basic-page></basic-page>
    
  </main-layout>

  <main></main>
</template>

<style scoped></style>
