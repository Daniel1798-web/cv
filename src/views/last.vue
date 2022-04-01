<template>
    <div class="padre-last" v-for="logo in whatsapp" :key="logo">
        <div class="hijo-last">

    <section class="section-1">
            <div class="sec-div">
           <a target="_blank" href="https://wa.me/543516838934"> <img class="la" v-on:click="move" :src="logo.ruta"></a>   
          <h2 class="numero">351-683-8934</h2>
        </div>
    </section>

    <section class="section-2">
        <div class="section-div2">

        <a href="mailto:danrieloto@gmail.com"> 
            <img class="la" v-on:click="move2" :src="gmail"> </a>
            <div class="dm">
           <h2 class="mail"  >  danrieloto@gmail.com    </h2>
            </div>
        </div >     
    </section>
        

    <section class="section-3">
        <div class="section-div3">
            <a href="#"> <img class="la" v-on:click="mo" :src="ubicacion"> </a>
            <h2 class="ubi" > Córdoba,Centro    </h2>
        </div>
    </section>

    </div>

</div>


</template>

<script>
//import App from '../App.vue'

export default{
  //components: { App },
    name:"last",

    data(){
        return{

            whatsapp:[{  name:"whatsapp", ruta:require("@/assets/icons/whatsapp.png")}],
            gmail:require("@/assets/icons/correo-electronico.png"),
            ubicacion:require("@/assets/icons/ubi.png"),
            mostrar:false,
            mostrar2:false,
            mostrar3:false,
        }
    },

    methods:{

        move()
            {
            this.mostrar = !this.mostrar
            console.log("gola")
            },

            move2()
            {
                    this.mostrar2 = !this.mostrar2
            console.log("gola")
            },

            mo()
            {
                alert("Ubicación:Cordoba,Centro")
            },

    },
}

</script>

<style lang="scss" scoped>


@import url('@/estilos/lastStyle.scss');

@import url('@/estilos/laptops/lastLaptop.scss');

@import url('@/estilos/phone/lastPhone.scss');

</style>