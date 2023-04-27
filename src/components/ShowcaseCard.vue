<template>
    <div id="card" class="col-12 col-sm-6 col-lg-3 mb-4 position-relative">
        <img :src="image" :alt="title" class="img-fluid rounded-2">
        <div class="position-absolute description text-white text-center d-flex flex-column justify-content-end rounded-2">
            <h3 class="text-capitalize fw-bold">{{ title }}</h3>
            <span class="text-uppercase mb-3">{{ category }}</span>
        </div>
    </div>
</template>

<script>
    export default {
    name: 'ShowcaseCard',
        props:['image', 'title', 'category']
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
#card{
    transition: 1s;
    &:hover{
        scale: 1.15;
        z-index: 1000;
    }
    .description{
        top: 0;
        width: calc(100% - 1.5rem);
        height: 100%;
        background: $hover-bg;
        opacity: 0%;
        transition: 1s;
    }
    &:hover .description{
        opacity: 85%;
        cursor: pointer;
    }
}

</style>