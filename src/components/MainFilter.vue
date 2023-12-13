<script>


// IMPORTS

import axios from 'axios';
import { store } from '../store';

// /IMPORTS

export default {
  props: [],
  components: {},
  data() {
    return {
      store,

    }
  },
  created() {
    axios.get(store.searchArchetypeURL).then(response => {
      store.archetypesArray = response.data;
    })
  },
  methods: {

  },
  mounted() { },
}
</script>

<template>
  <div class="col-md-4 py-4 ms-3">
    <select id="inputFilter" class="form-select" aria-label="inputFilter" v-model="store.chosenArchetype"
      @change="$emit('tellToSearchIt')">
      <option value="" selected disabled>Select Archetype</option>
      <option value="">All</option>
      <option v-for="archetype in store.archetypesArray" :value="archetype.archetype_name">{{ archetype.archetype_name }}
      </option>

    </select>
  </div>
</template>

<style lang="scss" scoped>
// USES



// /USES

.form-select {
  width: 250px;
}
</style>

