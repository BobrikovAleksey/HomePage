<template>
  <Header />
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/>
</template>

<script>
import Header from '@/components/header/Header.vue';

export default {
  name: 'Home',
  components: {
    Header,
  },
};
</script>

<style lang="sass">
@import assets/styles/index
</style>
