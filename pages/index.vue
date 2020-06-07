<template>
  <div class="container">
    <h1 class="container__text">NUXTJS TEMPLATE</h1>
    <button>CLICK ME PLEASE</button>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="scss">

 .container {
   height: 100vh;
   background: $primary-bg;
   @include flex-center;

    &__text {

      color: gold;
      font-size: rem(32px);

        @include mobile {

          color: purple;

        }

    }

 }

</style>
