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
    last
  }
}
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: hsl(180, 55%, 27%);

}

.h{
  background-color: #ffffff;
  margin: 0%;
  padding: 0%;
 
 
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
