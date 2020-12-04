<template>
  <header class="header">
    <Background />

    <div class="header__container">
      <div class="header__top">
        <Logo />

        <Menu />
      </div>

      <div class="header__content">
        <h2 class="header__text">Frontend <span>/</span> Backend</h2>

        <h1 class="header__title">РАЗРАБОТЧИК</h1>

        <a class="header__button" href="#">СВЯЗАТЬСЯ СО МНОЙ</a>
      </div>

      <div class="header__bottom">
        <ScrollIndicator />
      </div>
    </div>
  </header>
</template>

<script>
import Background from '@/components/header/Background.vue';
import Logo from '@/components/Logo.vue';
import Menu from '@/components/header/Menu.vue';
import ScrollIndicator from '@/components/header/ScrollIndicator.vue';

export default {
  name: 'Header',
  components: {
    Background,
    Logo,
    Menu,
    ScrollIndicator,
  },
};
</script>

<style scoped lang="sass">
@import ../../assets/styles/vars, ../../assets/styles/mixins

.header
  height: 100vh
  font-weight: 200
  text-align: center
  background-color: $HeaderBackground
  position: relative
  &__container
    max-width: 1280px
    height: 100%
    color: $HeaderColor
    +flexDir(column)
    padding: 32px
    position: relative
    margin: 0 auto
  &__top
    +flexJcSb
  &__content
    height: 50vh
    +flexDirCC(column)
    flex-grow: 1
  &__bottom
    +flexJcC
    padding-top: 16px
  &__text
    +GaramondSerif
    +textCSWS($HeaderColor, 28px, 400, 2px)
    font-style: italic
    & span
      +MontserratSansSerif
  &__title
    +KronaOneSansSerif()
    +textCSWS($HeaderColor, 80px, 600, 3px)
    margin-top: 16px
  &__button
    +CommissionerSansSerif
    +textCSWS($HeaderColor, 18px, 400, 2px)
    border: 2px solid $HeaderColor
    display: flex
    margin-top: 24px
    padding: 1em 2em
    &:hover
      color: $TextColor
      background: $HeaderColor
      box-shadow: 0 0 8px 0 $HeaderColor
</style>
