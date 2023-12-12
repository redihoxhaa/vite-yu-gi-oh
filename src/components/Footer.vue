<script>
// IMPORTS

import Logo from './Logo.vue';

// /IMPORTS

export default {
  props: [],
  components: { Logo },
  data() {
    return {

    }
  },
  methods: {},
  mounted() { },
}
</script>

<template>
  <footer>
    <div class="container d-flex justify-content-between align-items-center py-4">
      <span>Qui finisce la pagina sennò sembra brutto</span>
      <Logo />
    </div>
  </footer>
</template>

<style lang="scss" scoped>
// USES
@use '../assets/scss/partials/variables' as *;
// /USES

footer {
  background-color: $secondary-color;
  color: white;
}
</style>
