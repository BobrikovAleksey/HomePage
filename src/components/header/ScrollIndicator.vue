<template>
  <button class="scroll-indicator" type="button">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 22 34">
      <path class="scroll-indicator__button"
            d="M11,33L11,33C5.5,33,1,28.5,1,23V11C1,5.5,5.5,1,11,1h0c5.5,0,10,4.5,10,10v12C21,
                 28.5,16.5,33,11,33z">
      </path>
    </svg>

    <span class="scroll-indicator__dot"></span>
  </button>
</template>

<script>
export default {
  name: 'ScrollIndicator',
};
</script>

<style scoped lang="sass">
@import ../../assets/styles/vars, ../../assets/styles/mixins

$width: 30px
$height: 48px

.scroll-indicator
  z-index: 21
  transform: translateX(-50%) translateY(-50%)
  cursor: pointer
  overflow: hidden
  width: $width
  height: $height
  background: none
  border-radius: 15px
  display: flex
  position: relative
  +marginTL($height / 2, $width / 2)
  &:hover
    background-color: $HeaderColor
    box-shadow: 0 0 8px 0 $HeaderColor
  &:hover .scroll-indicator__dot
    background-color: $HeaderBackground
  & svg
    width: 100%
    height: 100%
  &__button
    transition: fill 350ms ease 0ms
    +animation(1500ms, 1, mouse)
    fill: rgba(255, 255, 255, 0)
    stroke: $HeaderColor
    stroke-dasharray: 200
    stroke-dashoffset: 100
    stroke-width: 2px
    position: relative
  &__dot
    z-index: 11
    transition: all 500ms ease 0ms
    +animation(1500ms, infinite, indicator)
    animation-timing-function: linear
    animation-delay: 1s
    opacity: 0.05
    width: 6px
    height: 6px
    background-color: $HeaderColor
    border-radius: 50%
    display: block
    +absoluteTL(50%, 50%)

@keyframes indicator
  0%, 10%
    opacity: 0.05
    transform: translateX(-50%) translateY(-250%)
  50%
    opacity: 1
    transform: translateX(-50%) translateY(-25%)
  100%, 90%
    opacity: 0.05
    transform: translateX(-50%) translateY(200%)

@keyframes mouse
  0%, 33%
    stroke-dasharray: 100
  100%
    stroke-dasharray: 200
</style>
