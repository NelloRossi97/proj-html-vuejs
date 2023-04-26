<template>
    <div class="divider d-flex my-5">
        <div class="left me-2"></div>
        <div class="right"></div> 
    </div>
    
</template>

<script>
    export default {
        name: 'Divider'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
.divider{
    height: 5px;
}
.left{
    width: 10px;
    background: $gradient-primary;
    border-radius: 50px;
}

.right{
    width: 50px;
    background: $gradient-primary;
    border-radius: 50px;
}
</style>