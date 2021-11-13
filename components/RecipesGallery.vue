<template>      
      <!--Images, cards, grid system-->
      <!--images that are looped through here and are imported to recipes.vue page-->
      <div class="container">
        <div class="row"> 
            
          <div class="figure text-center bg-light border m-4 col"
                v-for="mep of meal"
                :key="mep.id"
                :mep="mep"
               >
              <div id="myPic">
                <!--animate meal name, fade in and out when click image-->
                <transition name="fade">
                <h5 v-if="show" class="px-5 py-2 text-center" display-4>{{mep.strMeal}}</h5>
                </transition> 
                <figure >                      
                <button v-on:click="show = !show">
                    <img class="figure-img rounded-top img-max py-3" :src="mep.strMealThumb" :alt="mep.strMeal" />                     
                </button>
                    <figcaption class="figure-caption px-2 pb-3 text-center">Category: {{mep.strCategory}}</figcaption>                    
                </figure>
                <p class="px-4 py-2"><b>Cooking instructions:</b> {{mep.strInstructions}}</p>
              
              </div>
          </div> 
         
        </div>
      </div>
      
</template>


<script>
export default {
  //prop validation
    props:{
      meal:{
        type:Array,
        required:true,
      }
    },
    data() {
      return {
         show: true,
         count: 0 }
    }
  
}
</script>


<style lang="scss" scoped>
button {
  border: none;
}
.img-max {
  max-width: 150px;
}
#main-pic {
  max-height: 380px;
  max-width: auto;
}

.active #myPic{
  border: 15px solid lightblue;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}

.fade-enter-active, .fade-leave-active {
  transition: all 1s ease-in-out;
}
</style>