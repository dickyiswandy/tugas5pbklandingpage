<template>
    <q-toolbar>
      <q-btn flat round icon="menu" @click="toggleDrawer" />
      <q-toolbar-title>
        <div class="text-h6">Nyx SuperCars</div>
      </q-toolbar-title>
      <q-space />
      <q-btn flat round icon="shopping_cart" />
      <q-btn flat round icon="account_circle" />
    </q-toolbar>
  
    <q-toolbar class="q-pa-none">
      <q-tabs
        v-model="currentTab"
        dense
        class="bg-primary text-white"
        align="left"
        indicator-color="white"
      >
        <q-tab name="home" icon="home" label="Home" />
        <q-tab name="produk" icon="shopping_bag" label="Produk" />
        <q-tab name="tentang-kami" icon="info" label="Tentang Kami" />
        <q-tab name="kontak" icon="contact_support" label="Kontak" />
      </q-tabs>
    </q-toolbar>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentTab: 'home'
      };
    },
    methods: {
      toggleDrawer() {
        this.$refs.leftDrawer.toggle();
      }
    }
  }
  </script>
  
  <style scoped>
  .q-toolbar {
    background-color: blue;
    color: white;
  }
  
  .q-tabs {
    background-color: blue;
  }
  
  .q-tab {
    font-weight: bold;
  }
  
  .q-tab .q-icon {
    color: white;
  }
  
  .text-h6 {
    font-size: 1.25rem;
    font-weight: 500;
  }
  </style>
  