<template lang="html">
  <router-link :to="{ name: '', params: {} }" class="link">
    {{ text }}
  </router-link>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: null
    },
    to: {
      type: String,
      default: null
    }
  }
}
</script>

<style lang="scss" scoped>
  .link {
    color: $d-gray;
    text-decoration: none;
    position: fixed;
    display: flex;
    transition: color .35s;
    font-size: 16px;
    line-height: 22px;

    @media screen and (max-width: $lg) {
      font-size: 14px;
      line-height: 20px;
    }

    &::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: -2px;
      left: 0;
      background-color: $white;
      transform-origin: bottom right;
      transition: width 0.35s ease-out;
    }

    &:hover {
      color: $white;

      &::after {
        width: 100%;
        transform-origin: bottom left;
      }
    }
  }
</style>
