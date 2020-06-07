<template>
  <div class="container">
    <h1 class="container__text">NUXTJS TEMPLATE</h1>
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
   background: hotpink;

    &__text {

      color: gold;

    }

 }

</style>
