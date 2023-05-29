<script>
    export default
    {
        name    : "AppHeader",
        methods :
        {
            nav_menu()
            {}
        }
    }
</script>

<template>
    <!-- NAV BAR TOP (MENU)-->
    <header class="std_flex">

        <a href="/" class="std_flex">
            <img src="img/avada-music-logo-retina.png" alt="Logo header">
        </a>

        <nav class="std_flex">

            <!-- RICORDARSI DI RENDERE NAV PRESENTE NEL MENU APERTO O CHIUSO -->
            <button id="nav_menu_btn" type="button" class="fs-2" v-on:click="nav_menu()">
                <i id="compressed_menu" class="fa-solid fa-bars"></i>
            </button>

        </nav>

    </header>

</template>

<style scoped lang="scss">

    
    @use "../assets/style/main.scss" as *;

    header
        {
        position: sticky;  /*Causa la sua staticità durante lo scroll insieme ad index*/
        top: 0;
        z-index: 999;
        width: 100%;
        height: $header_height_basic;
        padding: 0 $header_x_padding;
        border: 3px solid yellow;

            a
            {
            height: 100%;

                img
                {
                height: 80%;
                object-fit: contain;
                border: 3px solid white;
                } 
            }

            nav
            {
                #nav_menu_btn
                {
                border: none;
                background-color: transparent;

                    #compressed_menu
                    {
                    color: $nav_menu_color;
                    }
                }
            } 
        }
</style>
