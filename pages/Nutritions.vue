<template>
  <div class="nutritions bg-warning pb-5" style="--bs-bg-opacity: .1">
    <!--import header from Header.vue-->
    <app-header></app-header>
    <div class="m-3 p-3 text-center">
<<<<<<< HEAD
      <h3 class="display-5 text-secondary pt-2 pb-3">{{title}}</h3>
=======
      <h3 class="display-5 text-secondary pt-2 pb-3">Nutritions</h3>
>>>>>>> d1e0da4c169c5b5cb8fdce2f89539680e4bea587
      <img id="main-pic" class="img-fluid rounded-top" 
      src="../static/assets/tomatoes-cut.jpg" alt="tomatoes">
    </div>
    <!--import accordion items from Accordion.vue -->
    <app-accordion></app-accordion>
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import Accordion from '../components/Accordion.vue';

export default {
  components: {
    'app-header': Header,
    'app-accordion': Accordion
  },
  data() {
    return{
<<<<<<< HEAD
    title:'Nutritions'      
    }    
  },
  head() {
      return {
        title: this.title,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'A place for nutrition information'
          }
        ]
      }
    }
=======
    
      
    }
    
  }
>>>>>>> d1e0da4c169c5b5cb8fdce2f89539680e4bea587
}
</script>

<style lang="scss" scoped>
.img-max {
  max-width: 300px;
}
#main-pic {
  max-height: 380px;
  max-width: auto;
}
</style>