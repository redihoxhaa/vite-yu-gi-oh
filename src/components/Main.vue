<script>
// IMPORTS
import MainFilter from './MainFilter.vue';
import MainCardList from './MainCardList.vue';


// /IMPORTS

export default {
  props: [],
  components: { MainFilter, MainCardList },
  data() {
    return {

    }
  },
  methods: {},
  mounted() { },
}
</script>

<template>
  <main>
    <div class="container">
      <MainFilter />
      <div class="nested container p-5">
        <MainCardList />
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
// USES

@use '../assets/scss/partials/variables' as *;

// /USES

main {
  background-color: $main-color;

  .nested.container {
    background-color: white;
  }
}
</style>
