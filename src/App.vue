<script>
import AppMain from "./components/AppMain.vue";
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
//STORE.JS
import { store } from "./store"

export default{
    name        : "App",
    components  : 
    {
      AppHeader,
      AppMain,
      AppFooter
    },
    data()
    {
      return {
        store
      }
    },
    mounted()
    {
      document.addEventListener("scroll", event => { this.store.is_scrolled = (window.scrollY != 0); });
    },
    methods:
    {
      
    }
}    
</script>


<template>
    <div id="web_page">

      <div id="layout-under">
        <img src="img/home_slider.jpg" alt="">
      </div>

      <!-- COMPONENT CONTAINER -->
      <div id="overlay">
        <AppHeader/>
        <AppMain/>
        <AppFooter/>
      </div>
    
    </div>

</template>

<style scoped lang="scss">
    //RICORDARSI CHE ABBIAMO UTILIZZATO FOGLIO STILE SCSS IN TUTTI I COMPONENTI /STYLE
    @use "./assets/style/main.scss" as *;

    #web_page
    {
      
      #layout-under{
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        height: 100vh;

        img
        {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
    }
</style>

