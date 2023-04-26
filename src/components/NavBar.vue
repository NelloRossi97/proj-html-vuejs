<template>
    <nav class="fixed-top">
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
        <div class="my-nav d-flex flex-column flex-xl-row justify-content-between align-items-center mx-5 my-4 text-uppercase">
            <div>
                <img src="/images/logo-text.png" alt="logo">
            </div>
            <div>
                <ul class="nav">
                    <li class="nav-item" v-for="link in navbar">
                        <a href="" class="nav-link">{{ link }}</a>
                    </li>
                </ul>
            </div>
            <div class="d-none d-xl-block">
                <ButtonPrimary :text="'purchase'"/>
                <i class="fa-solid fa-magnifying-glass ms-3"></i>
            </div>
        </div>
    </nav>
    
</template>

<script>
import { navbar } from '../data/data.js';
import ButtonPrimary from './ButtonPrimary.vue';
    export default {
    name: 'NavBar',
    components: {
        ButtonPrimary
    },
    data() {
        return {
                navbar
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
nav{
    background-color: $bg-primary;
    z-index: 1000;
    box-shadow: 0 4px 44px 0 rgba(0,0,0,.14);
}
.my-nav{
    i{
        color: $contrast-color;
    }
}
.nav-link{
    color: $header-footer-text-color;
    &:hover{
        color: $contrast-color;
    }
}
.topbar{
    background-color: $topbar-bg;
}
</style>