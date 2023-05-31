<script>
    export default
    {
        name        : "AppSpItem",
        props       : ['csi_menu_item'],
        data()
        {
            return {
            }
        },
        methods     :
        {
        }
    }
</script>

<template>
    <button type="button">{{csi_menu_item.text}}</button>
</template>

<style scoped lang="scss">
    
    @use "../assets/style/main.scss" as *;
    
</style>