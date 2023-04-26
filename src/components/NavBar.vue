<template>
    <nav class="d-flex justify-content-between align-items-center mx-5 my-4 text-uppercase">
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
        <div>
            <ButtonPrimary :text="'purchase'"/>
            <i class="fa-solid fa-magnifying-glass ms-3"></i>
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
i{
    color: $contrast-color;
}
.nav-link{
    color: $header-footer-text-color;
}
</style>