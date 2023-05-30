<script>
import { store } from "../store";
export default
    {
        name: "AppHeader",
        data()
        {
            return {
                store
            }
        },
        methods :
        {
            nav_menu()
            {}
        }
    }
</script>

<template>
    <!-- NAV BAR TOP (MENU)-->
    <header class="std_flex" :class="(store.is_scrolled) ? ('scrolled') : ('')">
        <a href="/" class="std_flex">
            <img src="img/avada-music-logo-retina.png" alt="Logo grande">
        </a>
        <!-- MENU OPEN/CLOSE -->
        <nav class="std_flex">
            <button id="nav_menu_btn" type="button" class="fs-2" v-on:click="nav_menu()">
                <i id="compressed_menu" class="fa-solid fa-bars"></i>
            </button>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@use "../assets/style/main.scss" as *;

header {
    position: sticky; /*Causa la sua staticità durante lo scroll insieme ad index*/
    top: 0;
    z-index: 999;
    width: 100%;
    height: $header_height_basic;
    padding: 0 $header_x_padding;
    transition: all 0.33s;

    &.scrolled {
        height: $header_height_scrolled;
        background-color: $header_bg_color;
    }

    a {
        height: 100%;

        img {
            height: 80%;
            object-fit: contain;
           
        }
    }

    nav {
        #nav_menu_btn {
            border: none;
            background-color: transparent;

            #compressed_menu {
                color: $nav_menu_color;
            }
        }
    }
}
</style>
