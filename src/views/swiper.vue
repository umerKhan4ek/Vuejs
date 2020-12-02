<template>
    <div class="mt-15 mb-10">
           <v-btn
      :disabled="dialog1"
      :loading="dialog1"
      class="white--text"
      color="purple darken-2"
      @click="dialog1 = true"
    >
      Start loading one
    </v-btn>
         <v-dialog
      v-model="dialog1"
      hide-overlay
      persistent
      width="300"
      lazy          
    >
      <v-card
        color="primary"
        dark
      >
        
                      <div id="one ">
  <v-app id="inspire "  class="black">
    <v-btn dark class="black mt-16 pt-16" @mousemove="Click()"> {{valueDeterminate}}</v-btn>
    <v-progress-linear class="mt-16 pt-4" v-model="valueDeterminate"></v-progress-linear>
  </v-app>
</div>
          <v-progress-linear
            indeterminate
            color="white"
            class="mb-0"
          ></v-progress-linear>
        
      </v-card>
    </v-dialog>

    </div>
</template>

<script>
    export default {
         data () {
    return {
      valueDeterminate: 0,
      total: 90,
      timeOut: 0,
      iteraciones: 90,
          dialog1: false,
    }
  },
         mounted(){

  },
      watch: {
      dialog1 (val) {
        if (!val) return
        setTimeout(() => (this.dialog1 = false), 4000)
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
  }
    }
</script>

<style  scoped>
 
 

#one {
  background: rgba(0, 0, 0, 0.733) !important;
  padding: 20px;
  transition: all 0.2s;
  animation: mm 4s forwards;

 
}


h2 {
  font-weight: bold;
  margin-bottom: 15px;
    color: white;
    background: #20262E !important;

}

del {
 background:black;
}
.back{
    background: brown;
}


</style>