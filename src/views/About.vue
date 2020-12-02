<template>
  <div class="about">
   
 

         <div class="ff">
          <img src="/01hero.jpg" alt="Avatar" class="image">
          <div class="overlay">
          <a class="text">Hello World</a>
          </div>
        </div>
   
  <v-row class="pa1" dark>
    <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
        <h1 id="tex" class=" headline white-text " >SNAKERS</h1>
        <h2 id="tex2">EVERSET</h2>
        </v-card>
  </v-row>
  <v-row class="pa2">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >SNAKKERS </h2>
   <h1 id="tex">EVERSET</h1>
   <h2 id="tex2">RED ROSE</h2>
 </v-card>
  </v-row>
    <v-row class="pa3">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >RED ROSE </h2>
   <h1 id="tex">RED ROOM</h1>
   <h2 id="tex2">ONLY DANCE</h2>
 </v-card>
  </v-row>

   <v-row class="pa4">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >RED ROSE </h2>
   <h1 id="tex">RED ROOM</h1>
   <h2 id="tex2">FOREST</h2>
 </v-card>
  </v-row>

   <v-row class="pa5">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >RED ROSE </h2>
   <h1 id="tex">FOREST</h1>
   <h2 id="tex2">ONLY DANCE</h2>
 </v-card>
  </v-row>
   <v-row class="pa6">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >FOREST </h2>
   <h1 id="tex">BLACK BOOK</h1>
   <h2 id="tex2">HANNAH</h2>
 </v-card>
  </v-row>
   <v-row class="pa7">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >BLACK BOOK</h2>
   <h1 id="tex">HANNAH</h1>
   <h2 id="tex2">CROSS BIKE</h2>
 </v-card>
  </v-row>

   <v-row class="pa8">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >HANNAH </h2>
   <h1 id="tex">CROSS BIKE</h1>
   <h2 id="tex2">COLOR DUST</h2>
 </v-card>
  </v-row>

   <v-row class="pa9">
     <v-card color="transparent" class=" pa-16 ma-16 elevation-0">
     <h2 id="tex2"  >RED ROSE </h2>
   <h1 id="tex">ROBOT</h1>
   <h2 id="tex2">ONLY DANCE</h2>
 </v-card>
  </v-row>
 
  </div>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: '/01hero.jpg',title:'SNEAKES'
          },
          {
            src: '/02hero.jpg',title:'EVERSER'
          },
          {
            src: '/03hero.jpg',title:'SKJDDS'
          },
          {
            src: '/04hero.jpg',title:'EVERSER'
          },
        ],
      }
    },
  }
</script>
    <style  scoped>


    .image {
  display: block;
  width: 50%;
  height: 50%;
}

.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #008CBA;
  overflow: hidden;
  width: 0;
  height: 50%;
  transition: .5s ease;
}

.ff:hover .overlay {
  width: 50%;
}

.text {
  color: black;

  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  white-space: nowrap;
}

/* .pa1 {
  background: url('/01hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa2 {
  background: url('/02hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa3 {
  background: url('/03hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa4 {
  background: url('/04hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa5 {
  background: url('/05hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa6 {
  background: url('/06hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa7 {
  background: url('/07hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa8{
  background: url('/08hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa9 {
  background: url('/09hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
.pa10 {
  background: url('/10hero.jpg') 
    no-repeat center center fixed !important;
  background-size: contain;
  width:100%;
  height: 800px;
}
#tex{
  font-size: 60px !important;
  font-weight:800 !important ;
  font-family: 'Oswald', sans-serif !important;
  animation: mytra 3s ;
  opacity: 1;
  color:white !important;
}
@keyframes mytra {
0% {opacity: 0;transform: translate(0px,-40px) }
25% {opacity: 0.3;transform: translate(0px,-30px)}
50% {opacity: 0.5;transform: translate(0px,-20px) }
75% {opacity: 0.8;transform: translate(0px,-10px)}
100% {opacity: 1;transform: translate(0px,0px)}
}
  #tex2 {
  color: black;
  -webkit-text-fill-color: transparent; /* Will override color (regardless of order) */
  /* -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: wheat;
   font-size: 60px !important;
  font-weight:800 !important ;
  
 
} */

    </style>
