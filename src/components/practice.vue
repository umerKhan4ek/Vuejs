<template>
  <v-container fluid class="grey lighten-5">

        <v-app id="inspire">
    <v-card
      flat
      tile
    >
      <v-window
        v-model="onboarding"
        vertical
      >
        <v-window-item
          v-for="n in items"
          :key="`card-${n}`"
       
        >
          <v-card
            color="grey"
            height="700px"
            @mousewheel="next"
          >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
             <v-btn
          text
          @click="next"
        >
          <v-icon>mdi-chevron-right</v-icon>
        </v-btn>
            <v-img  width="800px" height="700px" :src="n.src"></v-img>
             <v-btn
          text
          @click="prev"
        >
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
        
            </v-row>
          </v-card>
        </v-window-item>
      </v-window>
  
      <v-card-actions class="justify-space-between">
       
        <v-item-group
          v-model="onboarding"
          class="text-center"
          mandatory
        >
        
        </v-item-group>
       
      </v-card-actions>
    </v-card>
  </v-app>   
  
  </v-container>
</template>
<script>
export default {
    data(){
        return{
             length: 3,
    onboarding: 0,
            items:[   {
          src:'/01hero.jpg',
        },
        {
          src:'/02hero.jpg'
        },
        {
          src:'/03hero.jpg'
        },
        {
          src:'/04hero.jpg'
        },
        {
          src:'/05hero.jpg'
        },
        {
          src:'/06hero.jpg'
        },]
        }
    },
     methods: {
    next () {
      this.onboarding = this.onboarding + 1 === this.length
        ? 0
        : this.onboarding + 1
    },
    prev () {
      this.onboarding = this.onboarding - 1 < 0
        ? this.length - 1
        : this.onboarding - 1
    },
  },
}
</script>

<style scoped>
.bounce-enter-active{
    animation:roll-in 2s;
     
}
.bounce-leave-active{
    animation: roll-in 2s reverse;
     
}
@keyframes roll-in {
    0%{transform:scale(0) rotateZ(0deg) translateX(-250px)}
    100%{transform:scale(1) rotateZ(360deg) translateX(0px)}
    }
</style>