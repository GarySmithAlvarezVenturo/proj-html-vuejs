<script>
import { store } from "../store";
import AppMenuMng from "./AppMenuMng.vue"

export default
    {
    name        : "Comp_Header",
    components  :
    {
        AppMenuMng
    },
        
        data() {
            return {
                store,
                nav_icon:
                {
                    menu_class: 0,
                    is_horizontal: true,
                    category: 0,
                    menu_items:
                        [
                            {
                                text: 'fa-solid fa-bars',
                                is_active: true
                            }
                        ]
                }
            };
        },
        
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
            <AppMenuMng 
            :menu_class = "nav_icon.menu_class"
            :category = "nav_icon.category"
            :is_horizontal="nav_icon.is_horizontal"
            :menu_items = "nav_icon.menu_items"
            />
        </nav>

    </header>

</template>

<style scoped lang="scss">
@use "../assets/style/main.scss" as *;

header {
    position: sticky;
    /*Causa la sua staticità durante lo scroll insieme ad index*/
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
            color: $nav_menu_color;

            &:hover {
                color: $nav_menu_hover_col;
            }
        }
    }
}
</style>
