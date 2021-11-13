<template>
    
        <!--carousel items that are looped through here and are imported to Home.vue page-->
        <div class="m-5 p-3">
           <a href="#">
            <b-carousel id="carousel" class="carousel slide carousel-fade" pause="false" wrap="true" data-bs-touch="false" data-bs-ride="carousel" @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
                <div class="carousel-indicators">
                <button type="button" data-bs-target="#carousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
                <button type="button" data-bs-target="#carousel" data-bs-slide-to="3" aria-label="Slide 4"></button>
                <button type="button" data-bs-target="#carousel" data-bs-slide-to="4" aria-label="Slide 5"></button>
                <button type="button" data-bs-target="#carousel" data-bs-slide-to="5" aria-label="Slide 6"></button>
                </div>
          
        <div class="container">
            <div class="carousel-inner">
                <div v-for="ingredient in ingredients" :key="ingredient.id">
                <div class="carousel-item">
                    <img :src="ingredient.image" class="d-block w-100" :alt="ingredient.name" />
                    <div class="carousel-caption text-secondary" style="--bs-bg-opacity: .1">
                    <h4>{{ingredient.name}}</h4>                 
                    </div>
                </div>
                </div>
            </div>
         </div>
            
                <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
                </button>
            </b-carousel>
            </a>
        </div> 




</template>


<script>
import lettuceRS from '../static/assets/lettuceRS.jpg';
import tomatoesRS from '../static/assets/tomatoesRS.jpg';
import riceRS from '../static/assets/riceRS.jpg';
import gingerRS from '../static/assets/gingerRS.jpg';
import cinnamonRS from '../static/assets/cinnamonRS.jpg';
import lemonRS from '../static/assets/lemonRS.jpg';

export default {
    data() {
        return{
         ingredients:[
     {id:'1',
         name:'Lettuce',
     image:lettuceRS, 
     },
     {id:'2',
         name:'Tomatoes', 
     image:tomatoesRS, 
     },
     {id:'3',
         name:'Rice', 
     image:riceRS, 
     },
     {id:'4',
         name:'Ginger',
     image:gingerRS, 
     },
     {id:'5',
         name:'Cinnamon',
     image:cinnamonRS,  
     },
     {id:'6',
         name:'Lemon', 
     image:lemonRS,    
     } 
    ]   
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