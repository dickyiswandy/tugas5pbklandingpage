<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated>
      <navbar />
    </q-header>
    <q-page-container>
      <q-page class="q-pa-md">
        <carousel />
      </q-page>
    </q-page-container>
    <Footer />
  </q-layout>
</template>

<script>
import Carousel from './components/Corousel.vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Carousel,
    Navbar,
    Footer
  }
}
</script>

<style>
/* Tambahkan gaya khusus Anda di sini */
</style>
