<template>
  <div class="home">
    <!--import header from Header.vue-->
    <app-header></app-header>
    <!--apply v-if and v-else -->
     <div>
          <div class="d-grid gap-2 col-4 m-3 mx-auto" display-2 mb-3>First time visitor?</div>
          <div class="d-grid gap-2 col-4 mx-auto">
          <b-button class="btn btn-success me-md-2" type="button" v-on:click="yes = !yes">Yes</b-button>         
          </div>
          <p v-if="yes" class="d-grid gap-2 col-4 m-3 mx-auto" display-4 mb-3>Welcome!</p>
          <p v-else></p>

      </div>
    <app-carousel></app-carousel> 
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import Carousel from '../components/Carousel.vue';
export default {
  components: {
    'app-header': Header,
    'app-carousel': Carousel
  },
  data() {
    return{
     yes: false,
     no: false,      
    }    
  }
}
</script>

<style lang="scss" scoped>
.main {
    padding: 2rem;
  padding: 2rem;
}
//main page
.carousel-inner {
  width: 100%;
  height: auto;
  max-height: 500px;
  border-radius: 5px;
}
.carousel-caption {
  top: 0;
  bottom: auto;
}

</style>


