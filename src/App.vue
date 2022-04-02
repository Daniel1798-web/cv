<template class="black">

  

<baner/>
<datos />

<last />



</template>

<script>
import baner from './views/baner.vue'
import datos from '@/views/datos.vue'
import last from '@/views/last.vue'

export default {
  name: 'App',
 
  
  components: {
    baner,
    datos,
    last,
    
  },
  data(){
    return{
      tema:false,
      boto:false,
    }

    
  },

  methods:{
        sec(){
          this.tema = !this.tema
          console.log("soy app")
          this.boto = !this.boto
        }
    }
 
}
</script>

<style >
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: hsl(180, 55%, 27%);
        min-height: 100vh;
   
       

        

      
  
  } 


   

@import url('@/estilos/appStyle.scss');

  
@media (min-width:540px){ 
@import url('@/estilos/phone/appPrueba.css');
}
  


</style>
