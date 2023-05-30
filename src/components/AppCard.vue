<script>
    export default
    {
        name        : "AppCard",
        props       : ['current_card', 'index'],
        methods:
        {
            set_card_classes()
            {
                if ((this.index == 0) || (this.index == 3))
                    return "horizontal";
                else if ((this.index == 4) || (this.index == 5))
                    return "vertical_with_grow";
            }
        }
    }
</script>

<template>
    <div class="card" :class="set_card_classes()">
        
    </div>
</template>

<style scoped lang="scss"> 
    @use "../assets/style/main.scss" as *;
    
</style>