<template>
    <section class="mx-3 d-flex flex-column flex-lg-row align-items-center justify-content-between">
        <div class="left">
            <Divider/>
            <h2 class="fs-1 fw-bold my-5"> Our recent <span>web designs</span>  & some examples of past <span>projects</span> </h2>
            <Divider/>
        </div>
        <div class="right d-flex align-items-end h-100">
            <p class="mt-5">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind
                texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language
                ocean.Separated they live in Bookmarksgrove.Far far away, behind the word mountains, far from the
                countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove.
            </p>
        </div>
    </section>
</template>

<script>
import Divider from './Divider.vue';
    export default {
    name: 'Showcase',
        components:{Divider}
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
.left{
    width: 45%;
    .divider{
        margin-top: 0 !important;
        margin-bottom: 0 !important;
    }
    h2{
        span{
            color: $contrast-color;
        }
    }
}
.right{
    width: 50%;
}


</style>