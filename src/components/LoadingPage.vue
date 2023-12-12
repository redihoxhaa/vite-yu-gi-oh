<script>
// IMPORTS

import Logo from './Logo.vue';

// /IMPORTS

export default {
  components: { Logo },
  data() {
    return {
      bigLogo: "big-logo",
    }
  },
  methods: {},
  mounted() { },
}
</script>

<template>
  <div class="loading-page d-flex flex-column align-items-center justify-content-center">
    <h2>Sto caricando..</h2>
    <img src="../assets/img/spinner.gif" alt="Spinner" class="my-4">
    <Logo :logoWidth="bigLogo" />
  </div>
</template>

<style lang="scss" scoped>
// USES
@use '../assets/scss/partials/reset' as *;

// /USES
.loading-page {

  width: 100vw;
  height: 100vh;

  img {
    width: 40px;
  }

}
</style>
