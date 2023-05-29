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
    <!-- NAV BAR TOP -->
    <header class="fixed-top vh-100 container-fluid">

        <nav class="fixed-top std_flex px-5">

            <a href="/" class="std_flex">
                <img src="img/avada-music-logo-retina.png" alt="Logo header">
            </a>

            <!-- BOTTONE DA MODIFICARE -->
            <button id="nav_menu_btn" type="button" class="fs-2" v-on:click="nav_menu()">
                <i class="fa-solid fa-bars"></i>
            </button>

        </nav>

    </header>

</template>

<style scoped lang="scss">

    
    @use "../assets/style/main.scss" as *;

    header
    {
        background-image: url(img/home_slider.jpg);
        background-size: cover;
        nav
        {
            height: $nav_height_transparent;
            border: 3px solid rgb(25, 243, 6);
            a
            {
                height: 100%;
                img
                {
                    height: 70%;
                    object-fit: contain;
                    border: 1px solid rgb(245, 9, 205);
                }
            } 
            #nav_menu_btn
            {
                background-color: transparent;
                border: none;
                i
                {
                    color: $nav_menu_btn_color; 
                } 
            }
        }
    }

</style>
