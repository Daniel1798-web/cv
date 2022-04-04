<template  >
<div class="padre "   >
  <div class="marco">
   <img class="picture" src="@/assets/icons/p1.png">
    
    <div class="cont">
        <h2 class="proyeh2">Proyectos</h2>
         <a target="_blanck" href="https://stock20.netlify.app/">
     <img class="pictureAlmacen" src="@/assets/almacen.jpg">
        </a> 

         <a target="_blanck" href="https://stock20.netlify.app/">
     <img class="pictureSuper" src="@/assets/descarga.jpg">
        </a>
        <div class="centrado">Stock</div>
        <ul class="proye2">
            
            <li class="proye"></li>
    </ul>
    </div>
        
  </div>
    <div class="sobremi">
        <h1 >sobre mi</h1>
        <p class="letras" >{{presentacion}}</p>
        
                 <div class="cont2" >
     <h2 class="proyePhone">Proyectos</h2>
        <ul class="proyePhone2">
            <li class="proyePhone3"><a target="_blanck" href="https://stock20.netlify.app/"><img class="pictureAlmacen" src="@/assets/almacen.jpg"></a></li>
                   <a target="_blanck" href="https://stock20.netlify.app/">
                    <img class="pictureSuper" src="@/assets/descarga.jpg"> </a>
        </ul>
    </div>


    </div>
     

    

   <div class="espacio">
     
</div>
    


<div class="tecnologias">
    <h1 class="te" >Tecnologías</h1>
        <div class="lista-div" v-for="icon in icono" :key="icon"   @mouseleave="icon.enseñar = false">
            <img  :class="icon.clase" :src="icon.ruta"  @mouseover="icon.enseñar = true"  v-on:click="sh" > 
                <p class="ti" v-show="icon.enseñar">{{icon.name}}</p>
            
        </div>
       
    </div>

     <div class="tecnologias2" >
        <h1 class="te">Tecnologías</h1>

        <div class="lista-div" v-for="icon in icono" :key="icon" >
         
        <img 
        :class="icon.clase"
        :src="icon.ruta" 
        v-on:click="sh"  @mouseover="icon.enseñar = true" @mouseleave="icon.enseñar = false" > 
           <p class="ti" v-show="icon.enseñar">{{icon.name}}</p>
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
                th:false,
                icono:[
                    
                    {
                        name:"vue",
                        v:"V-3.2.31",
                        clase:"cosa1",
                        ruta:require("@/assets/icons/vue.png"),
                        enseñar:false,
                    },

                    {
                        name:"angular",
                        v:"V-12.1.4",
                         clase:"cosa2",
                        ruta:require("@/assets/icons/angular.png"),
                        id:1,
                       enseñar:false

                    },

                    {
                        name:"MongoDB",
                        clase:"cosa3",
                        ruta:require("@/assets/icons/mongodb.png"),
                        enseñar:false,
                    },

                    {
                        name:"TypeScript",
                        v:"V-4.3.4",
                        clase:"cosa4",
                        ruta:require("@/assets/icons/typescript.png"),
                        enseñar:false,
                    },

                    {
                        name:"sass",
                        v:"V-7.0.1",
                        clase:"cosa5",
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
                   this.icono.enseñar= !this.icono.enseñar
                    console.log("hola")
                   
                },
                selected(){
                console.log("hi")
                this.tema = !this.tema
                },
                tecName(){
                    this.enseñar = !this.enseñar
                },
                
              

           

        },

    }

</script>

<style  scoped>


@import url('@/estilos/datosStyle.scss');
@import url('@/estilos/laptops/datoslaptop.scss');
@import url('@/estilos/phone/datosPhone.scss');



</style>
