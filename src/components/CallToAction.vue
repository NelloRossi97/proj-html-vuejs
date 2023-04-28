<template>
    <section class="m-5">
        <div class="row mx-5 justify-content-between">
            <div id="email" class="col-12 col-md-6 d-flex flex-column align-items-center p-5 rounded-4 ms-5">
                <span class="text-capitalize mb-2">are you ready</span>
                <h2 class="mb-5 fw-bold fs-1">Start a New Project</h2>
                <div class="position-relative">
                    <input type="email" placeholder="Enter Your Email Adress" class="rounded-5">
                    <button class="text-uppercase position-absolute rounded-4">submit</button>
                </div>
                
            </div>
            <div id="start" class="col-12 col-md-6 d-flex flex-column align-items-center p-5 rounded-4 me-5">
                <span class="text-capitalize">what are you waiting for</span>
                <h2 class="mb-5 fw-bold fs-1">Start a New Project</h2>
                <ButtonSecondary :text="'start now'"/>
            </div>
        </div>
    </section>
</template>

<script>
import ButtonSecondary from './ButtonSecondary.vue';
    export default {
    name: 'CallToAction',
    components: {
        ButtonSecondary
    }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

#email{
    background: $gradient-secondary;
    width: 45%;
    color: $bg-primary;
    height: 35vh;
    div{
        width: 80%;
    }
    input{
        width: 100%;
        height: 40px;
        border: none;
        padding-left: 20px;
        background: #505050;
    }
    button{
        border: none;
        background: transparent;
        height: 85%;
        color: $text-grey;
        font-weight: bold;
        right: 4px;
        top: 3px;
        &:hover{
            background: $gradient-secondary;
        }
    }
}
#start{
    background: $hover-bg-reverse;
    width: 45%;
    color: $bg-primary;
    height: 35vh;
}
</style>