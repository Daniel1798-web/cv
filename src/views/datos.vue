<template  >
<div class="padre "  v-bind:class=" tema ? 'negro' : 'blanco' " >
  <div class="marco">
   <img class="picture" src="@/assets/icons/p1.png">
   
        
  </div>
    <div class="sobremi">
        <h1 >sobre mi</h1>
        
        <p class="letras" v-bind:class="tema ? 'letrasdark' : 'letras' ">{{presentacion}}</p>
        
    </div>

    

   <div class="espacio">
</div>
    


    <div class="tecnologias" >
        <h1 class="te">Tecnologías</h1>
        <div class="lista-div" v-for="icon in icono" :key="icon">
                        <p v-show="enseñar">{{icon.name}}</p>

        <img  class="im-icon" :src="icon.ruta"  v-on:click="sh" > 
        </div>
    </div>

     <div class="tecnologias2" >
        <h1 class="te">Tecnologías</h1>
        <div class="lista-div" v-for="icon in icono" :key="icon">
            <p v-show="enseñar">{{icon.name}}</p>
        <img  class="im-icon" :src="icon.ruta" v-on:click="sh"  > 
        </div>
    </div>


</div>



</template>

<script>
    export default{
        name:"datos",
      

        

        data(){
            return{
                sol:require("@/assets/icons/modo.png"),
                tema:false,
                enseñar:false,
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
                selected(){
                console.log("hi")
                this.tema = !this.tema
                }
                
              

           

        },

    }

</script>

<style  scoped>


@import url('@/estilos/datosStyle.scss');
@import url('@/estilos/laptops/datoslaptop.scss');
@import url('@/estilos/phone/datosPhone.scss');



</style>
