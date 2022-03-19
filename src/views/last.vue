<template>
 
    <div class="padre-last" v-for="logo in whatsapp" :key="logo">
        <div class="hijo-last">

            <section class="section-1">
            
                <div class="sec-div">
           <a href="#"> <img class="l" v-on:click="move" :src="logo.ruta"> </a>

          <h2 class="numero"  v-show="mostrar" > 351-683-8934</h2>
            </div>
            </section>

            <section class="section-2">
           <div class="section-div2">
        <a href="#"> <img class="l" v-on:click="move2" :src="gmail"> </a>
        <h2 class="mail"  v-show="mostrar2" > danrieloto@gmail.com</h2>


         </div >
                
        </section>
        
        <section class="section-2">
            <div class="section-div2">
                <a href="#"> <img class="l" v-on:click="move3" :src="ubicacion"> </a>
                <h2 v-show="mostrar3"  class="mail" > Córdoba,Centro</h2>

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

            move3()
            {
                    this.mostrar3 = !this.mostrar3
            console.log("gola")
            },

    },
}

</script>

<style scoped>

    .padre-last{
        
    background-color: rgb(67, 136, 121);
    display: inline;
    width: 100%;
    height: 80px;
    padding: 10px;
    bottom: 0;
    
    display: grid;
    grid-template-columns: 1fr ;
    color: rgb(255, 255, 255);
     position: fixed;
    border:2px solid rgb(45, 241, 232);
   
 
    }

    .hijo-last{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
           
            

    }


    

   .l{
       max-width: 70px;
    }

    .numero{
       font-size-adjust: none;
       font-size: 25px;
       margin-left: 5px;
       color:hsl(180, 55%, 27%);
     
    }

  .section-div2{
      display: flex;
      justify-content: start;
  }

  .mail{
     
      text-align: center;
        max-width: 70px;
        margin-left: 5px;
  }

    .sec-div{
        display: flex;
    }

    .section-2{
    color: hsl(180, 55%, 27%);
    font-family:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    text-align: center;
    
    }
    .info{
    list-style: none;
    
    }   
</style>