<template>
 <link href="../estilos/phone/headerPhone.scss" rel="stylesheet" media="screen and (min-width: 768px)"> 

<div class="f">

    <header class="fre">
        
  <section class="header-icon">
      <div class="icons">
          <a target="_blanck" :href=rutaLink><img class="logo-link" src="@/assets/icons/link.png" alt="logo"></a>
          <a target="_blanck" :href=rutaGit><img class="logo-link" src="@/assets/icons/github.png"></a>
          
      </div>
  </section>
  <nav class="na">
    <section class="logo-container" >
      <a href="#"><img  src="@/assets/icons/logo2.png"></a>
    </section>
   <section class="profile">
       <h1 >FRONT-END DEVELOPER JUNIOR</h1>
    </section>
  </nav>
</header>
      
    
</div>

</template>

<script>
export default{
    name:"baner",

    data(){
        return{
            rutaGit:"https://github.com/Daniel1798-web",
            rutaLink:"https://www.linkedin.com/in/daniel-oto-diaz-45282a21b/"
        }
    }
}
</script>




<style lang="scss" scoped>

@import url('@/estilos/headerStyle.scss');

@import url('@/estilos/phone/headerPhone.scss');

</style>