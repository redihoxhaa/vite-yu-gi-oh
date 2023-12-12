<script>
// IMPORTS



// /IMPORTS

export default {
  props: ['logoWidth'],
}
</script>

<template>
  <div class="pic-container mx-4" :class="logoWidth">
    <img src="/logo.png" alt="">
  </div>
</template>

<style lang="scss" scoped>
// USES

// /USES

.pic-container {
  width: 52px;

  img {
    width: 100%;
  }
}
</style>
