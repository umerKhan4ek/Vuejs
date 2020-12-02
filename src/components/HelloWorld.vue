<template>
  <div>
    

    <div id="app">
  <v-app id="inspire float-sm-left float-md-left">
    <v-container fluid pt-0 absolute >
     
    <v-layout row wrap justify-start>
      <v-flex>
        
         <v-carousel   prev-icon="mdi-light mdi-arrow-left" next-icon="mdi-light mdi-arrow-right"  vertical height="" shrink-on-scroll
      prominent 
      class="swipe"
         hide-delimiters>
          <v-carousel-item
           append 
            v-for="(item,i) in slides"
            :key="i"  
            :src="item.src"

           
          >

                    <v-container
                      fill-height
                      fluid
                      pa-0 ma-0 pb-3 

                    >
                      <v-layout fill-height align-center  >
                        <v-flex xs12>
                           <transition name="slide-fade" mode="out-in">
                          <v-card id="spa" color="transparent" class=" pa-16 ma-16 elevation-0">
                             <h2 id="tex2"  v-text ="item.text3"  > </h2>
                             
                          <h2 id="tex" class=" headline  " v-text ="item.text"  > </h2>
                             
                          <h1 id="tex2"  v-text ="item.text2"    > </h1>
                          </v-card>
                         </transition>
                        </v-flex>
                      </v-layout>
                    </v-container>

             </v-carousel-item>
           </v-carousel>
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</div>

 </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
     
      slides: [
        {
          src:'/01hero.jpg',text:'SNEAKERS',text2:'EVERSET'
        },
        {
          src:'/02hero.jpg',text:'EVERSET',text2:'RED ROOM',text3:'SNEAKERS'
        },
        {
          src:'/03hero.jpg',text:'RED ROOM',text2:'ONLY DANCE',text3:'EVERSET'
        },
        {
          src:'/04hero.jpg',text:'ONLY DANCE',text2:'FOREST',text3:'RED ROOM'
        },
        {
          src:'/05hero.jpg',text:'FOREST',text2:'BLACK BOOK',text3:'ONLY DANCE'
        },
        {
          src:'/06hero.jpg',text:'BLACK BOOK',text2:'HANNAH',text3:'FOREST'
        },
        {
          src:'/07hero.jpg',text:'HANNAH',text2:'CROSS BIKE',text3:'BLACK BOOK'
        },
        {
          src:'/08hero.jpg',text:'CROSS BIKE',text2:'ROBOT',text3:'HANNAH'
        },
        {
          src:'/09hero.jpg',text:'ROBOT',text2:'COLOR DUST',text3:'CROSS BIKE'
        },
        {
          src:'/10hero.jpg',text:'COLOR DUST',text2:'KATYA',text3:'ROBOT'
        },
        {
          src:'/11hero.jpg',text:'KATYA',text2:'ONLY DANCE',text3:'COLOR DUST'
        }
      ],

    }),

   
    
  }
</script>
<style scoped>


#tex{
  font-size: 60px !important;
  font-weight:800 !important ;
  font-family: 'Oswald', sans-serif !important;
  animation: mytra 1s ;
  opacity: 1;

}
@keyframes mytra {
0% {opacity: 0;transform: translate(0px,-40px);color: transparent  }

100% {opacity: 1;transform: translate(0px,0px);;}
}
  #tex2 {
  color: black;
  -webkit-text-fill-color: transparent; /* Will override color (regardless of order) */
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: wheat;
   font-size: 60px !important;
  font-weight:800 !important ;
  
 
}

#inspire{
  scroll-snap-type: mandatory;
}
.swipe{
  background-blend-mode: multiply !important;
  scroll-snap-align:start; 
}



/* 
.pa1 {
  background: url('/01hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 500px;
}
.pa2 {
  background: url('/02hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 500px;
}
.pa3 {
  background: url('/03hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 500px;
}
.pa4 {
  background: url('/04hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 500px;
} */
.v-btn .v-btn__content .v-icon {
        color: black !important;
    }


</style>
