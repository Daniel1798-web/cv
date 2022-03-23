<template >
<div class="padre ">
   
    <div class="sobremi">
        <h1 >sobre mi</h1>
        <p class="letras">{{presentacion}}</p>
        <h3>aqui mas cosas</h3>
        <div>
        <button>Proyecto1</button>
        </div>
    </div>

    

   <div class="espacio"></div>
    


    <div class="tecnologias" >
        <h1 class="te">Tecnologías</h1>
        <div class="lista-div" v-for="icon in icono" :key="icon">
        <img  class="im-icon" :src="icon.ruta" > 
        </div>
    </div>

     <div class="tecnologias2" >
        <h1 class="te">Tecnologías</h1>
        <div class="lista-div" v-for="icon in icono" :key="icon">
        <img  class="im-icon" :src="icon.ruta" > 
        </div>
    </div>


</div>



</template>

<script>
    export default{
        name:"datos",
      

        data(){
            return{
                tecnologi:false,
                  enseñar: false,
                icono:[
                    
                    {
                        name:"V-3.2.31",
                        ruta:require("@/assets/icons/vue.png"),
                        enseñar:false,
                    },

                    {
                        name:"V-12.1.4",
                        ruta:require("@/assets/icons/angular.png"),
                        id:1,
                        enseñar:false,

                    },

                    {
                        name:"MongoDB",
                        ruta:require("@/assets/icons/mongodb.png"),
                        enseñar:false,
                    },

                    {
                        name:"V-4.3.4",
                        ruta:require("@/assets/icons/typescript.png"),
                        enseñar:false,
                    },

                    {
                        name:"V-7.0.1",
                        ruta:require("@/assets/icons/sass.png"),
                        enseñar:false,
                    }
                
                ],
                presentacion:`Hola, me llamo Daniel. Empecé a estudiar 
                por mi cuenta Programación web hace dos años. De todas las tecnologías, 
                la que más me interesó fue JavaScript, 
                me encantó las infinitas posibilidades que ofrece y la cantidad de frameworks disponibles. 
                
                `
            }
        },
        methods:{
                animar(){
                  //setInterval(this.animacion,1000)
                    console.log("hola")
                },
                
                animar2(){
                    this.icono.id
                },

                changeTecnology(){
                    this.tecnologi = !this.tecnologi
                },

                sh(){
                   this.enseñar = !this.enseñar
                    console.log("hola")
                   
                },


        },

    }

</script>

<style  scoped>


@import url('@/estilos/datosStyle.scss');
@import url('@/estilos/phone/datosPhone.scss');



</style>
