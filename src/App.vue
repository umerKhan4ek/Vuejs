<template>
<div>
  
  <v-app class="na ">
     
     <v-layout
      align-center
      wrap 
        
    >
      <v-dialog 
      v-model="dialog1"
      hide-overlay
       fullscreen
       transition="dialog-bottom-transition"
      width="80%"
      persistent
        color="black"
       class="mt-16 pt-16"  
      lazy   >
       <div id="swipp">
      <v-card
        color="black"
        dark  class="mt-16 pt-16 " > 
           <v-app id="inspire" color="transparent"  class="transparent">
    <v-btn  height="auto" color="black" hide-overlay class=" dia3 elevation-0"  @mouseout="Click()"> <h1 class="About2">{{valueDeterminate}}</h1></v-btn>
    <v-progress-linear  class="ml-16 mr-15 " background-color="transparent lighten-5" v-model="valueDeterminate"></v-progress-linear>
  </v-app>
       
      </v-card>
       </div>
    </v-dialog>
  
     
    </v-layout>
     
     





    <v-app-bar
      app relative 
      color="transparent"
      class="elevation-0 pa-7"
      pa-5
      dark
    >
      <div class="d-flex align-center">
                  <v-img
                   alt="Vuetify Logo"
                  class="shrink mr-4"
                   contain
                   src="http://clapat.ro/themes/hervin-wordpress/wp-content/themes/hervin/images/logo-white.png"
                   transition="scale-transition"
                    width="40"
        />
        <!-- LEFT DIALOG BOX LEFT DIALOG BOX BOX LEFT DIALOG BOX LEFT DIALOG BOX -->
         <!-- LEFT DIALOG BOX LEFT DIALOG BOX BOX LEFT DIALOG BOX LEFT DIALOG BOX -->
          <!-- LEFT DIALOG BOX LEFT DIALOG BOX BOX LEFT DIALOG BOX LEFT DIALOG BOX -->
          <div class="left-dialog">
           
   <v-row justify="center">
          <v-dialog
                 v-model="dialog2"
                fullscreen
                 hide-overlay
                close-delay="200"
                open-delay="200"
                class="one fullone "
                 dark       
         >
     <template v-slot:activator="{ on, attrs }">
                 <v-btn
                  color="transparent"
                  dark
                 v-bind="attrs"
                 v-on="on"
                 class="elevation-0  "
        >
     <span class="font-weight-black ml-1 mr-1">+</span> 
                </v-btn>
      </template>
              <v-card>
               <v-toolbar
                 dark
                color="transparent"
                class="elevation-0 pa-7" 
        >
             <v-img
                 alt="Vuetify Logo"
                 class="shrink pr-2  "
                 contain
                 src="http://clapat.ro/themes/hervin-wordpress/wp-content/themes/hervin/images/logo-white.png"
                transition="scale-transition"
                 width="40"
        />
      <v-btn
               dark
                text
               @click="dialog2 = false"
              class=""
         >
              <h1> - </h1>
     </v-btn>
         <v-btn
              dark
              text
              @click="dialog2 = false"
             
          >
                              <span class="font-weight-bold">close </span>
         </v-btn>
          <v-spacer></v-spacer>
          <v-dialog
                 v-model="dialog"
                 fullscreen
                 hide-overlay
                 close-delay="200"
                 open-delay="200"
                class="one fullone "
                 dark
           >
 <template v-slot:activator="{ on, attrs }">
           <v-btn
                color="transparent"
                 dark
                  v-bind="attrs"
                 v-on="on"
                 class="elevation-0 "
        >
                       <v-spacer></v-spacer>
          <h2 class="mb-1 pr-2  font-weight-bold"> =</h2>
           </v-btn>
 </template>
           <v-card>
               <v-toolbar
          dark
          color="transparent"
          class="elevation-0 pt-7 pr-5 pl-7"
        >
     <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="http://clapat.ro/themes/hervin-wordpress/wp-content/themes/hervin/images/logo-white.png"
          transition="scale-transition"
          width="40"
     />
                   <v-spacer></v-spacer>
        <v-toolbar-items>
         <v-btn
                  dark
                  text
                 @click="dialog = false"
                 class="elevation-0"
         >
                         <v-icon>mdi-close</v-icon>
        </v-btn>
     </v-toolbar-items>
 </v-toolbar>
           <v-list
                 three-line
                 subheader
                  id="About"
                 class="listone "
        >
       <div class="animated"> <h4 >PORTOFOLIO</h4></div>
       <div class="animated2"><a>ABOUT</a></div>
       <div class="animated3"><a>STORIES</a></div>
        <div class="animated4"><a>CONTACT</a></div> 
    </v-list>
  </v-card>
 </v-dialog>
        <v-toolbar-items> 
      </v-toolbar-items>
  </v-toolbar>
      
        <v-list 
          three-line
          subheader
          id="About2"
          class=" ml-16 pl-16 mt-16   "
        >
   <div class="ss">
      <v-col class="shrink animated"  >
           <v-btn  flat
             elevation="0"
              class="mt-10 clicky large display-1"
              color="transparent" @mouseover="expand1 = true" @mouseleave="expand1=false"  >
             EVERSET
        </v-btn>
   <v-expand-x-transition>
          <v-card
              style="z-index:-1"
              v-show="expand1"
               height="150px"
               width="280px"
              class="mt-n16"
       >
         <img class="hhhh" src="/01hero.jpg" alt="" width="280px" height="150px"> 
      </v-card>
               </v-expand-x-transition>
 </v-col>
        </div>

     <div class="ss">
        <v-col class="shrink animated3"  >
             <v-btn  flat
             elevation="0"
             class="mt-10 clicky large display-1"
              color="transparent" @mouseover="expand3 = true" @mouseleave="expand3=false"  >
         RED ROOM
        </v-btn>
        <v-expand-x-transition>
          <v-card
             style="z-index:-1"
            v-show="expand3"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/03hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
        </v-expand-x-transition>
      </v-col>
        </div>
          <div class="ss">
           <v-col class="shrink animated4"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand4 = true" @mouseleave="expand4=false"  >
                         ONLY DANCE
        </v-btn>
        <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand4"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/04hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
        </v-expand-x-transition>
      </v-col>
        </div>
  <div class="ss">
           <v-col class="shrink animated5"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand5 = true" @mouseleave="expand5=false"  >
                      FOREST
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand5"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/05hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
   </v-expand-x-transition>
      </v-col>
        </div>
          <div class="ss">
           <v-col class="shrink animated6"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand6 = true" @mouseleave="expand6=false"  >
         BLACK BOOK
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand6"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/06hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
   </v-expand-x-transition>
      </v-col>
        </div>

   <div class="ss">
           <v-col class="shrink animated2"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand7 = true" @mouseleave="expand7=false"  >
                         HANNAH
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand7"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/07hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
   </v-expand-x-transition>
      </v-col>
        </div>
        <div class="ss">
           <v-col class="shrink animated2"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand8 = true" @mouseleave="expand8=false"  >
                        CROSS BIKE
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand8"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/08hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
   </v-expand-x-transition>
      </v-col>
        </div>
        <div class="ss">
           <v-col class="shrink animated2"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand9 = true" @mouseleave="expand9=false"  >
                         ROBOT
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand9"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/09hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
   </v-expand-x-transition>
      </v-col>
        </div>
          <div class="ss">
           <v-col class="shrink animated2"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand10 = true" @mouseleave="expand10=false"  >
                              COLOR DUST
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand10"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/10hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
   </v-expand-x-transition>
      </v-col>
        </div>
            <div class="ss mb-10">
           <v-col class="shrink animated2"  >
        <v-btn  flat
        elevation="0"
        class="mt-10 clicky large display-1"
          color="transparent" @mouseover="expand11 = true" @mouseleave="expand11=false"  >
                     KATYA
        </v-btn>
   <v-expand-x-transition>
          <v-card
          style="z-index:-1"
            v-show="expand11"
            height="155px"
            width="280px"
            class="mt-n16"
          >
         <img class="hhhh" src="/11hero.jpg" alt="" width="280px" height="155px"> 
          </v-card>
  </v-expand-x-transition>
      </v-col>
        </div>
            <!-- <div class="seg1  "><a class="animated " >SNEAKERS</a></div>
            <div class="seg2 "><a class="animated2" >EVERSET</a></div>
            <div class="seg3 "><a class="animated3">RED ROOM</a></div>
            <div class="seg4 "><a class="animated4">ONLY DANCE</a></div>
            <div class="seg5 "><a class="animated5">FOREST</a></div>
            <div class="seg6 " ><a class="animated6">BLACK BOOK</a></div>
            <div class="seg7 "><a  >HANNAH</a></div>
            <div class="seg8 "><a >CROSS BIKE</a></div>
            <div class="seg9 "><a >ROBOT</a></div>
            <div class="seg10 "><a >COLOR DUST</a></div>
            <div class="seg11 "><a >KATYA</a></div> -->
        <!-- <div  class="animated img1 "> <a >SNEAKERS</a></div>
        <div class="animated2 img2 mb-5"><a >EVERSET</a></div>
         <div class=" animated3 img3 mb-5"><a >RED ROOM</a></div>
         <div class="animated4 img4 mb-5"><a >ONLY DANCE</a></div>
          <div class="animated5 img5 mb-5"><a >FOREST </a></div>
           <div class="animated6 img6 mb-5"><a >BLACK BOOK</a></div>
            <div class="img7 mb-5"><a >HANNAH</a></div>
             <div class="img8 mb-5"><a >CROSS BIKE</a></div>
              <div class="img9 mb-5"><a >ROBOT</a></div>
               <div class="img10 mb-5"><a >COLOR DUST</a></div>
                <div class="img11"><a >KATYA</a></div> -->
        </v-list> 
      </v-card>
    </v-dialog>
  </v-row>
  </div>
           <span class="ml-4 font-weight-black">  All Projects</span></div>
                       <v-spacer></v-spacer>
           <span class="mr-4 font-weight-black">Menu</span>
      <!-- RIGHT DIALOG BOX RIGHT DIALOG BOX RIGHT DIALOG BOX -->
       <!-- RIGHT DIALOG BOX RIGHT DIALOG BOX RIGHT DIALOG BOX -->
        <!-- RIGHT DIALOG BOX RIGHT DIALOG BOX RIGHT DIALOG BOX -->

       <div class="">
          <v-row justify="center">
            <v-dialog
              v-model="dialog"
               fullscreen
              hide-overlay
              close-delay="200"
              open-delay="200"
              class="one fullone "
              dark  
    >
   <template v-slot:activator="{ on, attrs }">
       <v-btn
               color="transparent"
               dark
              v-bind="attrs"
              v-on="on"
              class="elevation-0 " >
             <v-spacer></v-spacer>
    <h2 class="mb-1 pr-3 ml-2  font-weight-bold"> =</h2>
        </v-btn>
  </template>
      <v-card>
        <v-toolbar
             dark
            color="transparent"
             class="elevation-0 pt-7 pr-5 pl-7" >
     <v-img
             alt="Vuetify Logo"
             class="shrink mr-3"
              contain
             src="http://clapat.ro/themes/hervin-wordpress/wp-content/themes/hervin/images/logo-white.png"
             transition="scale-transition"
             width="40" />
    <v-spacer></v-spacer>
          <v-toolbar-items>
               <v-btn
                          dark
                          text
                         @click="dialog = false"
                        class="elevation-0"  >
                         <v-icon>mdi-close</v-icon>
                </v-btn>
          </v-toolbar-items>
        </v-toolbar>
       <v-list
              three-line
             subheader
             id="About"
             class="listone">
                  <div class="animated"> <h4 >PORTOFOLIO</h4></div>
                   <div class="animated2"><a>ABOUT</a></div>
                  <div class="animated3"><a>STORIES</a></div>
                  <div class="animated4"><a>CONTACT</a></div>
           </v-list>
      </v-card>
    </v-dialog>
  </v-row>
  </div>
    </v-app-bar>
          <v-main class="pad">
           <HelloWorld/>
           <practice/>
           <!-- <swiper/> -->
         <!-- <About/> -->
           </v-main>  
<v-card  >
      <v-footer
              absolute
              color="transparent" 
              class="font-weight-medium elevation-0" >
         <v-col
               class="text-center"
               cols="12" >
        
         </v-col>
    </v-footer>
  </v-card>
  </v-app>
  </div>
</template>
<script>
import HelloWorld from './components/HelloWorld';
// import practice from './components/practice';
// import swiper from './views/swiper'
// import About from './views/About';
export default {
  name: 'App',
  components: {
    HelloWorld,
    // practice
        // swiper
    // About 
  },
  data: () => ({
      dialog: false, dialog2:false, expand1: false, expand2:false,
       expand3:false, expand4:false, expand5:false, expand6:false, expand7:false,
       expand8:false, expand9:false, expand10:false, expand11:false, 
         dialog1: false,
          valueDeterminate: 0,
      total: 90,
      timeOut: 0,
      iteraciones: 90,


  }),
   watch: {
      dialog1 (val) {
        if (!val) return
        setTimeout(() => (this.dialog1 = false), 5600)
      },
     
    },
  methods:{
   async Click(){
     var arr = [];
     var sum = 0;   
     this.valueDeterminate = 0;
     
     // Set the sleep Interval based on initial total
     Object.defineProperty(this, 'sleepInterval', {value: 4000/this.total, writeable: false});
     
     await this.forEach(this.iteraciones, async (i) => {
        await this.Sleep(this.sleepInterval);
        arr.push(1);
        sum++;
        this.SetProgressBar(sum);
        clearTimeout(this.timeOut);
      })      
    },
    SetProgressBar(num) {
      if (num) {
        this.valueDeterminate = Math.round(this.Map(num));
      }
    },
    Map(value) {
      return ((value - 0) * (100 - 0)) / (this.total - 0) + 0;
    },
    async forEach(arr, callback){
      for(let i = 0; i < arr; i++){
        await callback(arr[i], i);
      }
    },
          Sleep(milisegundos) {
      return new Promise(resolve => this.timeOut = setTimeout(resolve, milisegundos));
    },
  },
  mounted(){
    this.dialog1=true;
    this.Click()
  }
  
};
</script>
<style scoped>
.dia3:hover {
  background: rgb(7, 6, 6)  !important;
  box-shadow: none;
  
}

#swipp {
    /* border-radius: 4px; */
    /* margin: 24px; */
    overflow-y: auto;
    height: 800px;
    pointer-events: auto;
    transition: 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    width: 100%;
    background: black;
   
    /* z-index: inherit; */
    /* box-shadow: 0px 11px 15px -7px rgba(0, 0, 0, 0.2), 0px 24px 38px 3px rgba(0, 0, 0, 0.14), 0px 9px 46px 8px rgba(0, 0, 0, 0.12); */
}
  .pad{
    padding-top:0px !important;
  }
   #About {
  color: black;
  display: block !important;
  -webkit-text-fill-color: transparent; /* Will override color (regardless of order) */
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: wheat;
   font-size: 60px !important;
  font-weight:700 !important ;
  text-align: center;
  margin-top: 150px;
  
}
#About2 {
  color: black;
  display: block !important;
  -webkit-text-fill-color: transparent; /* Will override color (regardless of order) */
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: wheat;
   font-size: 50px !important;
  font-weight:600 !important ;
  margin-top: 150px;
  opacity: 0.9; 
}
.About2 {
  color: black;
  display: block !important;
  -webkit-text-fill-color: transparent; /* Will override color (regardless of order) */
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: rgb(240, 238, 235);
   font-size: 50px !important;
  font-weight:600 !important ;
  margin-top: 150px;
  opacity: 0.9; 
}
.one{
  background: black !important;
}
.listone a:hover {
  -webkit-text-stroke-color: white;
    -webkit-text-stroke-width: 2px;
-webkit-text-fill-color: white;
animation: eee 0.7s ease-in-out   forwards;
opacity: 1;
}
@keyframes eee {
   0%{opacity: 0;}
   100%{opacity: 1;}
} 
.clicky:hover {
  -webkit-text-stroke-color: white;
    -webkit-text-stroke-width: 2px;
-webkit-text-fill-color: white;}

h4{
  -webkit-text-stroke-color: white;
    -webkit-text-stroke-width: 2px;
-webkit-text-fill-color: white;
}
.seg1 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;  
     padding:50px 10px 0px 10px; 
}
.seg1:hover {
    background-size: cover;
 background: url('/01hero.jpg') no-repeat right   transparent ; 
  animation: moveSlideshow 1s ease   forwards ;
     
}
.seg2 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px; 
         padding:40px 10px 0px 10px;     
}
.seg2:hover {
    background-size: cover;
 background: url('/01hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow2 1s ease   forwards ;
      padding:10px 10px 20px 10px; 
}
.seg3 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;      padding:40px 10px 0px 10px; 
}
.seg3:hover {
    background-size: cover;
 background: url('/02hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow3 0.9s ease   forwards ;
     
}
.seg4 {
    height: 180px; width: 300px; 
    text-align: start;
    background-size: 0px;   padding:40px 10px 0px 10px;
}
.seg4:hover {
    background-size: cover;
 background: url('/03hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow4 1s ease   forwards ;
     
}
.seg5 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;    padding:40px 10px 0px 10px; 
}
.seg5:hover {
    background-size: cover;
 background: url('/05hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow5 1s ease   forwards ;
     
}
.seg6{
    height: 180px; width: 300px;
    text-align: start; 
    background-size: 0px;   padding:40px 10px 0px 10px; 
}
.seg6:hover {
    background-size: cover;
 background: url('/04hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow6 1s ease   forwards ;
     
}
.seg7 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;    padding:40px 10px 0px 10px; 
}
.seg7:hover {
    background-size: cover;
 background: url('/04hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow7 1s ease   forwards ;
     
}
.seg8 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;   padding:40px 10px 0px 10px; 
}
.seg8:hover {
    background-size: cover;
 background: url('/08hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow8 1s ease   forwards ;
     
}
.seg9 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;   padding:40px 10px 0px 10px; 
}
.seg9:hover {
    background-size: cover;
 background: url('/09hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow9 0.9s ease   forwards ;
     
}
.seg10 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;   padding:40px 5px 0px 10px; 
}
.seg10:hover {
    background-size: cover;
 background: url('/10hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow10 0.9s ease   forwards ;
     
}
.seg11 {
    height: 180px; width: 300px;
    text-align: start;
    background-size: 0px;   padding:40px 5px 5px 1px; 
}
.seg11:hover {
    background-size: cover;
 background: url('/11hero.jpg') no-repeat right  transparent ; 
  animation: moveSlideshow11 0.9s ease   forwards ;
     
}
.listtwo a:hover {
  -webkit-text-stroke-color: white;
    -webkit-text-stroke-width: 2px;
-webkit-text-fill-color: white;}
.fullone{
  animation: fully 3s ease-in-out 0s  forwards ;
}
@keyframes fully {
  to{opacity: 0;}
  from{opacity:1}
}

.animated{
  animation-duration:1s;
  animation-fill-mode: both;
  animation-name: onetwo;
  -o-animation-fill-mode: forwards;
opacity: 0;
}

.animated2{
  animation-duration:1s;
  animation-fill-mode: both;
  animation-name: onetwo;
  -o-animation-fill-mode: forwards;
  animation-delay: 0.2s;
opacity: 0;
}

.animated3{
  animation-duration:1s;
  animation-fill-mode: both;
  animation-name: onetwo;
  -o-animation-fill-mode: forwards;
  animation-delay: 0.4s;
opacity: 0;
}
.animated4{
  animation-duration:1s;
  animation-fill-mode: both;
  animation-name: onetwo;
  -o-animation-fill-mode: forwards;
  animation-delay: 0.6s;
opacity: 0;
}
.animated5{
  animation-duration:1s;
  animation-fill-mode: both;
  animation-name: onetwo;
  -o-animation-fill-mode: forwards;
  animation-delay: 0.8s;
opacity: 0;
}
.animated6{
  animation-duration:1s;
  animation-fill-mode: both;
  animation-name: onetwo;
  -o-animation-fill-mode: forwards;
  animation-delay: 1s;
opacity: 0;
}
@keyframes onetwo {
  0%{ transform:translate3d(0,100%,0);  opacity: 0; }
  100%{ transform:translate3d(0,0,0) ;  opacity: 1;}}

.ss{
  width: 290px;
  height: 120px;
}
.zzz{
  height: 700px !important;
}
body {
  background: black;
  padding: 20px;
  font-family: Helvetica;
}

#one {
  background: black;
  border-radius: 4px;
  padding: 20px;
  transition: all 0.2s;
}

li {
  margin: 8px 0;
}

h2 {
  font-weight: bold;
  margin-bottom: 15px;
}

del {
  color: blue;
}

</style>