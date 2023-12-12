<script>
// IMPORTS



// /IMPORTS

export default {
  props: {
    img: String,
    archetype: {
      type: String,
      default: "Unknown"
    }, cardName: String
  },
  components: {},
  data() {
    return {

    }
  },
  methods: {},
  mounted() { },
}
</script>

<template>
  <div class="single-card">
    <div class="pic-container">
      <img :src="img" :alt="cardName">
    </div>
    <h5 class="text-center text-uppercase p-3">{{ cardName }}</h5>
    <p class="text-center p-3">{{ archetype }}</p>
  </div>
</template>

<style lang="scss" scoped>
// USES
@use '../assets/scss/partials/variables' as *;
@use '../assets/scss/partials/reset' as *;
// /USES

.single-card {
  background-color: $main-color;
  aspect-ratio: 9 / 19;

  h5 {
    color: white;
    font-size: 1rem;
  }

  p {
    font-size: 1.125rem;
  }

  .pic-container {

    img {
      width: 100%;
    }
  }

}
</style>
