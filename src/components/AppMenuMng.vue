<script>
    import AppItem from "./AppItem.vue";
    export default
    {
        name        : "AppMenuMng",
        components  : 
        {
            AppItem
        },
        props       : ['menu_class', 'is_horizontal', 'category', 'menu_items'],
        
    }
</script>

<template>

    <div class="menu_manager" :class="(!(is_horizontal) ? ('flex-column') : (''))">

        <AppItem v-for="(item, index) in menu_items" :key="index + menu_class" :csi_menu_item="item"
            :csi_category="category" :csi_menu_class="menu_class" />
    
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