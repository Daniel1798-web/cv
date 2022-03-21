<template>
<div >
  

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
     

}

body{
      
    background-color: rgb(255, 255, 255);
    padding: 0%;
    margin: 0%; 
   
    display: grid;
    gap: 1rem;
    grid-auto-rows: 2rem;
    grid-template-columns: repeat(auto-fill, minmax(min(100%, 50rem), 1fr));
   
    min-height: 100vh;
   
    position: relative;
    padding-bottom: 2em;
    
  }

 
  body::-webkit-scrollbar{
    width: 0px;
  }

.h{
  background-color: #ffffff;
  margin: 0%;
  padding: 0%;
 
 
}

.r{
  width:100% ;
  height: 150%;
  font-size: 150%;
}

  .square2{
    width: 20px;
    height: 20px;
    border-radius: 10px;
    background-color: black;
    box-shadow:  1px 1px  10px 10px rgb(30, 145, 139);

    animation-name: mymove;
    position: relative;
    animation-duration: 5s;
    animation-iteration-count: infinite;
}

@keyframes mymove{
    0% {top: 0px; left: 0px;}

    25%{top: 0px; left: 97%;}

    50%{top: 96%; left: 97%;}

    75%{top: 96%; left: 0px;}

    100%{top: 0px; left: 0px;}

}




</style>
