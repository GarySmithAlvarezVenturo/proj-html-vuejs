<script>
import AppItem from "./AppItem.vue";
import AppSpItem from "./AppSpItem.vue";
export default
    {
        name: "AppMenuMng",
        components:
        {
            AppItem,
            AppSpItem

        },

        props: ['menu_class', 'is_horizontal', 'category', 'menu_items'],

        methods     :
        {
            rebound_click(index_to_rebound)
            {
                this.$emit("rebounded",index_to_rebound);
            }
        }

    }
</script>

<template>

    <div class="menu_manager" :class="(!(is_horizontal) ? ('flex-column') : (''))" :style="((menu_class == 60) || (menu_class == 30)) ? ('gap: 0.75rem;') : ('')">

        <div          
         v-for="(item, index) in menu_items"
         :key="index + menu_class">
            <AppItem
             v-if="(menu_class != 30)"  
             :csi_menu_item = "item" 
             :csi_category = "category"
             :csi_menu_class = "menu_class" 
             :social_index = "index"
            />
            <AppSpItem
             v-else
             :cs_menu_item = "item"
             :cs_index = "index"
             @click_on_special = "rebound_click"
            />
        </div>
    
    </div>
    
</template>

<style scoped lang="scss">
    
    @use "../assets/style/main.scss" as *;

        .menu_manager
        {
            // height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
        
        }

</style>