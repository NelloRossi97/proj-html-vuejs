<template>
    <section class="d-flex flex-column flex-xl-row align-items-center position-relative">
        <div class="left">
            <div id="bg-img" class="d-none d-xl-block">
                <div class="filter"></div>
            </div>
            
            <img src="/images/lissa-durbin.jpg" alt="lissa durbin">
        </div>
        <div class="right">
            <h2 class="fw-bold fs-1 mt-5 mt-xl-0"> learn more about <br> our <span>missions</span>  </h2>
            <Divider/>
            <p class="mb-4">Far far away, behind the word mountains, far from the countries Vokalia and
    Consonantia, there live the blind texts. Separated they live in Bookmarksgrove
    right at the coast of the Semantics, a large language ocean.Separated they live
    in Bookmarksgrove.</p>
    <ButtonPrimary :text="'read more'"/>
        </div>
    </section>
</template>

<script>
import Divider from './Divider.vue';
import ButtonPrimary from './ButtonPrimary.vue';
    export default {
    name: 'LearnAbout',
    components: {
        Divider,
            ButtonPrimary
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
section{
    margin: 30vh 5vw;
    padding: 15vh 0;
    background-color: $bg-secondary;
    .left{
        width: 55%;
        overflow: hidden;
        #bg-img{
            position: absolute;
            z-index: 2;
            height: 70%;
            width: 45%;
            left: -100px;
            top: 40px;
            background-image: url('/images/learn-more-bg.jpg');
            background-size: cover;
            border-radius: 40px;
            .filter{
                width: 100%;
                height: 100%;
                z-index: 5;
                background: $hover-bg;
                opacity: 80%;
                border-radius: 40px;
            }
            
        }
        img{
            position: relative;
            width: 80%;
            border-radius: 20px;
            z-index: 10;
        }
    }
    .right{
        width: 45%;
        h2{
            span{
                color: $contrast-color;
            }
        }
    }
    }

</style>