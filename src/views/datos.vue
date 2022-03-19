<template >
<div class="padre ">
 

    <section>
         <div class="square2"></div>

 <div  >
        <img class="picture " src="@/assets/icons/p1.png" alt="foto personal">
        
     
         <h1>Datos personales</h1>
         <p >Nací en Málaga , me mude a Argentina con catorce años</p>
         
         

    </div>
    </section>
    
    <section class="sobremi">
        <h1>Sobre Mí</h1>
    
      
    <div class="sobremiText">


        <p class="letras">{{presentacion}}</p>
      
    
 
    </div>
    
    </section>
    
<div class="tecnologi-dad">
    <section class="listaTecnologias" @mouseover="sh()" @mouseout="sh()">
        <h1 >Tecnologías</h1>
        <div class="lista-div " v-for="icon in icono" :key="icon">
             
            <ul>
            <p v-show="enseñar " class="letras">{{icon.name}}</p>

            <img @click="sh()"  class="im-icon" :src="icon.ruta"> 
            

         
            </ul>
    
        </div>
    </section>
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
                presentacion:`Hola! me llamo Daniel  Empecé a estudiar por mi cuenta Programación web hace dos años
            de todas las tecnologías la que mas me intereso fue JavaScript,
            me encantó las infinitas posibilidades que ofrece  y la cantidad de frameworks disponibles `
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

<style  lang="scss" scoped>


.padre{
    display: grid;
    grid-template-columns: 1fr 2fr 1fr ;
    border-bottom:  2px solid black;
 
}

.container {
  position: relative;
  width: 50%;
}

.picture{
    width: 300px;
    border-radius: 20%;
}



.square{
    width: 20px;
    height: 20px;
    border-radius: 10px;
    background-color: black;
    animation-name: move;
    animation-duration: 2s;
    animation-iteration-count: infinite;
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


.hij{
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 100%;
}

.sobremi{
    text-align: center;
    background-color: rgb(255, 255, 255);
   animation-name: move;
    animation-duration: 10s;
    animation-iteration-count: infinite;
   
}



.sobremiText{
     display: flex;
    flex-wrap: wrap;
    font-size: 140%;
    color: #000;
}

.tecnologi-dad{
    box-shadow:  1px 1px  10px 10px rgb(30, 145, 139);
    height: 700px;
   display: flex;
    padding: 5px;
   flex-direction: column;
   margin-left: 100px;
   
   
}

@media (min-width: 400px){
    .tecnologi-dad{
        box-shadow:  1px 10px  20px 20px  rgb(30, 145, 139);
    height: 100%;
    width: 50%;
   display: flex;
    padding: 5px;
   flex-direction: column;
      margin-left: 150px;


    }
    
}

.listaTecnologias{
        margin-bottom: 20px;
  
}



.lista-div{
    list-style:  none;
    display: flex;
    height: 118px;
    
    


    
}



.agrandar{
    background-color: red;

}

.letras
{
    width: 100%;
    margin-bottom:5px;
    font-size: 20px;
    animation-name: colores;
    animation-duration: 5s;
    animation-iteration-count: infinite;
  
}

@keyframes colores {

    0%{
        color: rgb(53, 129, 125);
    }

    20%{
        color:rgb(22, 100, 74);
    }

    100%{
        color: rgb(89, 240, 220);
    }
    
}

.im-icon{
    width: 80px;
    text-align: right;
    display: flex;
flex-basis: auto;
flex-grow: 1 200px;
}



.im-icon:hover{
    width: 90px;
     animation-name: move;
    animation-duration: 2s;
    animation-iteration-count: infinite;
}
    

    @keyframes move {

        from{
            left: 0px;

        }

         to{
             width: 100%;
         }
        
    }






    

</style>
