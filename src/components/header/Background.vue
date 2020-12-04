<template>
  <div class="header__background"></div>
</template>

<script>
export default {
  name: 'Background',
};
</script>

<style scoped lang="sass">
@import ../../assets/styles/vars, ../../assets/styles/mixins

.header__background
  width: 100%
  height: 100%
  filter: brightness(0.40)
  background-image: url(../../assets/images/background-photo.jpg)
  background-size: cover
  background-position-x: center
  background-position-y: center
  background-repeat: no-repeat
  +absoluteTLSingle(0)
</style>
