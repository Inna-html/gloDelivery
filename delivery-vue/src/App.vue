<script setup>
import { ref } from 'vue';

import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Modal from './components/Modal.vue';
import FooterVue from './components/Footer.vue';

const isOpen = ref(false);

</script>


<template>

  <div class="page-wrapper">

      <Header @toggleModal="isOpen = !isOpen" />

      <main class="main">
          <router-view></router-view>
      </main>

      <Modal :isOpen="isOpen" @toggleModal="isOpen = !isOpen" />
      <Footer />

  </div>

</template>

<style scoped>
</style>


