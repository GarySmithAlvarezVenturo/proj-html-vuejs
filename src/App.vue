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
    }
}    
</script>


<template>
    <div id="web_page" class="container-fluid">
    <AppHeader/>
    <AppMain/>
    <AppFooter/>
    </div>

</template>

<style scoped lang="scss">
    //RICORDARSI CHE ABBIAMO UTILIZZATO FOGLIO STILE SCSS IN TUTTI I COMPONENTI /STYLE
    @use "./assets/style/main.scss" as *;

    #web_page
    {
      background-color: $web_page_bg_color;
    }

</style>

