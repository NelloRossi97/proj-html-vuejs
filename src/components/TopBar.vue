<template>
    <div class="topbar d-flex-column d-sm-flex text-center justify-content-between align-items-center p-2 text-white">
        <div class="ms-sm-5">
            <span>(001) 88451234 88455438</span>
        </div>
        <div class="me-sm-5">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter mx-4"></i>
            <i class="fa-brands fa-pinterest-p"></i>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'TopBar'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
.topbar{
    background-color: $topbar-bg;
}
</style>