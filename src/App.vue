<template>
<div class="padre" >
  

<heeader class="h" msg="tio"/>
<datos />

<last />


</div>
</template>

<script>
import heeader from './views/heeder.vue'
import datos from '@/views/datos.vue'
import last from '@/views/last.vue'

export default {
  name: 'App',
  components: {
    heeader,
    datos,
    last,
    
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
        display:inline-flex;

        

      
  
  } 
   

@import url('@/estilos/appStyle.scss');

  
@media (min-width:540px){ 
@import url('@/estilos/phone/appPrueba.css');
}
  


</style>
