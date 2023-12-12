<script>
import LoadingPage from './components/LoadingPage.vue';
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import axios from 'axios';
import { store } from './store.js';

export default {
  data() {
    return {
      store
    }
  },
  components: { LoadingPage, Header, Main, Footer },
  created() {
    axios.get(store.apiURL).then(response => {
      store.cards = response.data.data;
    })
  }
}
</script>

<template>
  <LoadingPage v-if="store.cards.length === 0" />
  <div class="else" v-else>
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<style lang="scss" scoped></style>
