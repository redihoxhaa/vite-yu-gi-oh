<script>
// IMPORTS
import MainSingleCard from './MainSingleCard.vue';
import { store } from '../store';
import axios from 'axios';


// /IMPORTS

export default {
  props: [],
  components: { MainSingleCard },
  data() {
    return {
      store,

    }
  },
  created() {
    axios.get(store.apiURL).then(response => {
      store.cards = response.data.data;
    })
  },
  methods: {},
  mounted() { },
}
</script>

<template>
  <header class="p-3">
    <h5>Found {{ store.cards.length }} cards</h5>
  </header>
  <ul class="d-flex flex-wrap">
    <li v-for="card in store.cards">
      <MainSingleCard :img="card.card_images[0].image_url_small" :archetype="card.archetype" :cardName="card.name" />
    </li>
  </ul>
</template>

<style lang="scss" scoped>
// USES

@use '../assets/scss/partials/variables' as *;
@use '../assets/scss/partials/reset' as *;

// /USES

header {

  background-color: $list-header-bg;

  h5 {
    font-size: 1rem;
    font-weight: bold;
    color: white;
  }
}

ul {

  gap: 25px;

  li {
    width: calc((100% - 100px) / 5);
  }
}
</style>
