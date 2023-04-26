<template>
    <section class="overflow-hidden d-flex flex-column justify-content-center ms-5">
        <div class="container">
            <span class="text-uppercase title">17 years of experience</span>
            <h2>We are a</h2>
            <h2>Web Design <span>Agency</span></h2>
            <p class="my-5 description">
            Far far away, behind the word mountains, far from the countries Vokalia and Consonantia,
            there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the
            Semantic; a large language ocean.Separated they live in Bookmarksgrove.
            </p>
            <ButtonPrimary :text="'read more'"/>
            <p class="text-uppercase my-5">
                <span>facebook</span> - 
                <span>instagram</span> -
                <span>youtube</span> -
                <span>twitter</span> 
            </p>
            <img class="d-xl-none w-75" src="/images/jumbo-img.png" alt="web designer">
        </div>
        
    </section>
</template>

<script>
import ButtonPrimary from './ButtonPrimary.vue';
    export default {
    name: 'Jumbotron',
    components: {
        ButtonPrimary
    }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

section{
    text-align: center;
}
.title{
    letter-spacing: 0.8rem;
}
h2{
    font-weight: bold;
    font-size: 4.6rem;
    span{
        color: $contrast-color;
    }
}
p{  
    color: $text-color;
    span{
        &:hover{
            text-decoration: underline;
        }
        cursor: pointer;
        font-weight: bold;
    }
}
@media screen and (min-width: 1200px) {
    section{
        background-image: url('/images/jumbo-img.png');
        background-position: calc(100% + 200px) 0;
        background-size: 60vw;
        background-repeat: no-repeat;
        text-align: left;
    }
    .description{
        max-width: 50%;
    }
}
</style>