<template>
  <div class="recipes">
    <!--import header from Header.vue-->
    <app-header></app-header>
    <div class="bg-danger" style="--bs-bg-opacity: .2">
            <div class="m-3 p-3 text-center">
<<<<<<< HEAD
                <h3 class="display-5 text-secondary pt-2 pb-3">{{title}}</h3>
=======
                <h3 class="display-5 text-secondary pt-2 pb-3">Recipes</h3>
>>>>>>> d1e0da4c169c5b5cb8fdce2f89539680e4bea587
                <img id="main-pic" class="img-fluid rounded-top" 
                src="../static/assets/sushi.jpg" alt="three raw samlmon sushi">
            </div>
    </div>             
      <!--import images from RecipesGallery.vue --> 
      <!--<app-recipesgallery :meals="meals"></app-recipesgallery> -->
    <section class="container" v-if="meals">
     <RecipesGallery
      v-for="meal of meals"
      :key="meal.id"
      :meal="meal"
      />
    </section>
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import RecipesGallery from '../components/RecipesGallery.vue';
import axios from 'axios';

export default {
  components: {
    'app-header': Header,
    RecipesGallery
  },

  data() {
    return{
     loading: true,     
     errored: false,
<<<<<<< HEAD
     meals: null,
     title: 'Recipes'         
=======
     meals: null         
>>>>>>> d1e0da4c169c5b5cb8fdce2f89539680e4bea587
    }    
  },
  //retrieve data from API
  mounted (){
    axios.get ('https://www.themealdb.com/api/json/v1/1/search.php?f=l')
      .then(response => (this.meals = response.data))
      .catch(error => {
      console.error(error)
      this.errored = true
      })
     .finally(() =>this.loading = false)
<<<<<<< HEAD
  },

  head() {
      return {
        title: this.title,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'A place for recipes'
          }
        ]
      }
    }
=======
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