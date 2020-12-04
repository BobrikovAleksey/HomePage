<template>
  <ul class="menu">
    <li class="menu__item menu__item_active">
      <router-link class="menu__link" to="/">
        <span>01.</span>
        <h3 class="menu__title">Главная</h3>

        <p class="menu__text">Краткое введение</p>
      </router-link>
    </li>

    <li class="menu__item">
      <router-link class="menu__link" to="#">
        <span>02.</span>
        <h3 class="menu__title">Обо мне</h3>

        <p class="menu__text">Немного о том, кто я и чем я люблю заниматься</p>
      </router-link>
    </li>

    <li class="menu__item">
      <router-link class="menu__link" to="#">
        <span>03.</span>
        <h3 class="menu__title">Портфолио</h3>

        <p class="menu__text">Несколько проектов, над которыми я работал</p>
      </router-link>
    </li>

    <li class="menu__item">
      <router-link class="menu__link" to="#">
        <span>04.</span>
        <h3 class="menu__title">Опыт</h3>

        <p class="menu__text">Мои навыки, квалификация и опыт работы в отрасли</p>
      </router-link>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Menu',
};
</script>

<style scoped lang="sass">
@import ../../assets/styles/vars, ../../assets/styles/mixins

.menu
  +MontserratSansSerif
  display: flex
  margin-left: 32px
  &__item
    margin-right: 32px
    &:last-of-type
      margin-right: 0
    &:hover
      background: $MenuBackground
      outline: 1px solid $HeaderColor
      box-shadow: 0 0 8px $HeaderColor
    &_active
      &:hover
        background: none
        outline: none
        box-shadow: none
      & .menu__link
        cursor: default
      & span
        border-bottom: 2px solid $HeaderColor
  &__link
    width: 196px
    height: 100%
    text-align: left
    +flexDir(column)
    padding: 12px
    & span
      +textCSWS($HeaderColor, 12px, 600, 2px)
      padding: 4px 0
  &__title
    +textCSWS($HeaderColor, 16px, 600, 2px)
    text-transform: uppercase
    margin: 24px 0 8px
  &__text
    +textCSWS($HeaderColor, 11px, 600, 1px)
    margin-bottom: 16px
</style>
