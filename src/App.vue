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

@import url('@/estilos/appStyle.scss');

@import url('@/estilos/phone/appPrueba.scss');

  


</style>
