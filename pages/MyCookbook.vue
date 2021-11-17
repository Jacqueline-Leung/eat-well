<template>
  <div class="my-cookbook">
    <!--import header from Header.vue-->
    <app-header></app-header>
     <!--Jumbotron-->
        <div class="jumbotron jumbotron-fluid background bg-success p-5">
            <div class="container">
<<<<<<< HEAD
                <div class="display-4 mb-3">{{title}}</div>
=======
                <div class="display-4 mb-3">My Cookbook</div>
>>>>>>> d1e0da4c169c5b5cb8fdce2f89539680e4bea587
                <p class="lead">Create your own cookbook, fill it with your favorite recipes.</p>
           </div>
        </div>
        <!--adding tooltips-->
        <div class="m-5 px-5">
<<<<<<< HEAD
            <h3>{{title}}</h3>
=======
            <h3>My cookbook</h3>
>>>>>>> d1e0da4c169c5b5cb8fdce2f89539680e4bea587
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae facere, quaerat cum <a href="#" data-bs-toggle="tooltip" title="vegan">cumque</a> harum culpa suscipit eum atque, voluptas soluta consequatur minus error autem quas! Molestias id ex labore dolor molestiae laboriosam veritatis, libero, excepturi animi neque eius? Minus perferendis saepe, harum perspiciatis <a href="#" data-bs-toggle="tooltip" title="lactose-free">aneque</a> quaerat error eveniet suscipit dignissimos, iure vitae porro sint exercitationem. Excepturi enim porro quibusdam modi nam architecto nobis.</p>
        </div>
        <!--grid system-->
        <!--import menu items from Menu.vue -->
        <app-menu></app-menu>
        

  </div>
</template>

<script>
import Header from '../components/Header.vue';
import Menu from '../components/Menu.vue';

export default {
  components: {
    'app-header': Header,
    'app-menu': Menu
  },
  data() {
    return{
<<<<<<< HEAD
      title: 'My Cookbook'
    }    
  },
  head() {
      return {
        title: this.title,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'A place for your favorite menu'
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
.jumbotron {
  background-image: url("../static/assets/cookbook-banner.jpg");
  background-size: cover;
}
</style>


