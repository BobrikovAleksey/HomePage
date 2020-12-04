<template>
  <router-link class="logo" to="/">
    <span>AB</span>
  </router-link>
</template>

<script>
export default {
  name: 'Logo',
};
</script>

<style scoped lang="sass">
@import ../assets/styles/vars, ../assets/styles/mixins

.logo
  cursor: pointer
  width: 80px
  height: 80px
  +textCSW($HeaderColor, 32px, 400)
  border: 2px solid $HeaderColor
  border-radius: 50%
  +flexCC
  &:hover
    box-shadow: 0 0 8px 0 $HeaderColor
  & span
    +ArizoniaCursive
    margin-left: -1px
</style>
