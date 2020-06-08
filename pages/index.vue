<template>
  <div class="container">
    <h1 class="container__text">NUXTJS TEMPLATE</h1>
    <h2>And it's content text...</h2>
    
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
   background: $secondary-bg;
   font-family: $main-font;

   @include max-container-width;

    &__text {

      color: purple;
      font-size: rem(32px);
      padding-top: 2rem;

      @include range (777px, 1111px) {
        color: blue;
      }

        

    }

 }

</style>
