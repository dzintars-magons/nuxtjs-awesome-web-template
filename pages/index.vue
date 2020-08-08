<template>
  <div class="navigation-page">

    <nav class="navigation">
      <ul class="navigation__list">
        <li> <nuxt-link to="/grid-examples">DISPLAY:GRID EXAMPLES</nuxt-link></li>
        <li><a href="#">COMING SOON</a></li>
        <li><a href="#">COMING SOON</a></li>
      </ul>
    </nav>

    <div class="main-container">
      <h1 class="main-container__text">NUXTJS TEMPLATE</h1>
        <h2>And it's content text...</h2>

      <div class="cards row">
        <div class="card-1 col-12 col-sm-6 col-md-4">
            <img class="card-1__image" src="https://picsum.photos/200" alt="">
            <p class="card-1__text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minima sunt quas culpa id ab blanditiis. Architecto quas autem magni hic doloribus, nam consequuntur eum a quis, minus, omnis modi neque!</p>
          </div>
          <div class="card-2 col-12 col-sm-6 col-md-4">
            <img class="card-2__image" src="https://picsum.photos/200" alt="">
            <p class="card-2__text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minima sunt quas culpa id ab blanditiis. Architecto quas autem magni hic doloribus, nam consequuntur eum a quis, minus, omnis modi neque!</p>
          </div>
          <div class="card-3 col-12 col-sm-6 col-md-4">
            <img class="card-3__image" src="https://picsum.photos/200" alt="">
            <p class="card-3__text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minima sunt quas culpa id ab blanditiis. Architecto quas autem magni hic doloribus, nam consequuntur eum a quis, minus, omnis modi miests haha!</p>
          </div>
      </div>
    </div>
  
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

.navigation {
  background-color: $secondary-bg;
  @include container;
  text-align: center;
  &__list {
    display: flex;
    align-items: flex-start;
    @include no-bullets;
  }
}

 .main-container {
  
   min-height: 100vh;
   background: $secondary-bg;
   font-family: $font-family;

   @include container;

   @include desktop-only {
     background: teal;
   }

    &__text {

      color: purple;
      font-size: $h2;
      padding-top: 2rem;

    }

 }

.card-1, .card-2, .card-3 {

  &__image {
    display: block;
    @include margin-x (auto);
  }
    
  &__text {
    width: 200px;
    @include margin-x (auto);
  }
 
}

</style>
