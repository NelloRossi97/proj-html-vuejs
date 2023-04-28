<template>
    <div id="endbar" class="mt-5 d-flex align-items-center justify-content-between">
        <div class="ms-5">
            <span>&copy; 2020 PHLOX BUSINESS THEME.</span>
        </div>
        <div class="me-5">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter mx-4"></i>
            <i class="fa-brands fa-pinterest-p"></i>
        </div>
        
    </div>
</template>

<script>
    export default {
        name: 'EndBar'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
#endbar{
    background: $gradient-secondary;
    height: 100px;
    color: $text-grey;
}
</style>