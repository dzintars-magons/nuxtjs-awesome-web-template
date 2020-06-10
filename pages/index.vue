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
   min-height: 100%;
   background: $secondary-bg;
   font-family: $font-family;

   @include max-container-width;

   @include desktop-only {
     background: teal;
   }

    &__text {

      color: purple;
      font-size: $h2;
      padding-top: 2rem;


        

    }

 }

</style>
