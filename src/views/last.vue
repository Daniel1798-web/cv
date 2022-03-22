<template>
 
    <div class="padre-last" v-for="logo in whatsapp" :key="logo">
        <div class="hijo-last">

            <section class="section-1">
            
                <div class="sec-div">
           <a target="_blank" href="https://wa.me/543516838934"> <img class="l" v-on:click="move" :src="logo.ruta"> </a>

          <h2 class="numero"  > 351-683-8934</h2>
            </div>
            </section>

            <section class="section-2">
           <div class="section-div2">
        <a href="#"> <img class="l" v-on:click="move2" :src="gmail"> </a>
        <h2 class="mail"  > danrieloto@gmail.com</h2>


         </div >
                
        </section>
        
        <section class="section-2">
            <div class="section-div2">
                <a href="#"> <img class="l" v-on:click="move3" :src="ubicacion"> </a>
      >    <h2 class="ubi" > Córdoba,Centro    </h2>

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

<style lang="scss" scoped>

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
       position: relative;
       font-size: 25px;
       margin-left: 5px;
       animation-name:mymove;
        animation-duration: 5s;
        max-width: 70px;
        animation-timing-function: cubic-bezier(0.075, 4.82, 1.165, 1);
        color: rgb(224, 178, 24);
        animation-iteration-count:1;
        position: relative
     
    }

  

  .section-div2{
      display: flex;
      justify-content: start;
  }

  .mail{
        font-size-adjust: none;
      max-width: 70px;
        position: relative;
       font-size: 25px;
        display:flex;
        animation-name:mymove;
        animation-duration: 5s;
        animation-timing-function: cubic-bezier(0.075, 0.82, 1.165, 1);
        color: rgb(224, 178, 24);
        animation-iteration-count:1;
        position: relative;
        
  }

  

  .square2{
    width: 20px;
    height: 20px;
    border-radius: 10px;
    background-color: black;
    box-shadow:  1px 1px  10px 10px rgb(30, 145, 139);

    animation-name: mymove;
    position: relative;
    animation-duration: 10s;
    
    animation-iteration-count: infinite;
}

  

  @keyframes mymove{ 0% {top: 0px; left: 100%; color: transparent } 25%{left: 0px; top: 50%;color: rgb(224, 178, 24); } 100%{left: 0px; top: 100%; color: rgb(224, 178, 24); }}

  @keyframes colores{ 0% {color: gold;} 25%{color: rebeccapurple; } 50%{color: tomato;} 100%{color: rgb(255, 22, 205);} }

  .ubi{
        text-align: center;
        position: relative;
        max-width: 70px;
        margin-left: 5px;
        animation-name:mymove;
        animation-duration: 5s;
        max-width: 70px;
        animation-timing-function: cubic-bezier(0.075, 0.82, 1.165, 1);
        color: rgb(224, 178, 24);
        animation-iteration-count:1;
        position: relative;
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

    @media(max-width:540px){
    .ubi{
        color:transparent;
        animation-name:none;
        font-size-adjust: none;
        position: relative;
        font-size: 25px;
        
    }
      .ubi:hover{
        animation: none;
    }

    

    .mail{
        color: transparent;
        animation-name:none;
        font-size-adjust: none;
        position: relative;
        font-size: 25px;
        display: flex;

    }
      .mail:hover{
        animation: none;
    }

     

    .numero{
        color: transparent;
        animation-name:none;
        font-size-adjust: none;
        position: relative;
        font-size: 25px;
    }
    .numero:hover{
        animation: none;
    }

     
    
      @keyframes colores{ 0% {color: transparent;} 25%{color: transparent; } 50%{color: transparent;} 100%{color: transparent;} }


    }
</style>