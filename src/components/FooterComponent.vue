<template>
    <footer class="mt-5">
        <div class="row mx-5">
            <div class="col-12 col-sm-6 col-lg-3">
                <img src="/images/logo-text.png" alt="Logo">
                <p class="my-5">While the lovely valley teems with vapour
                    around me, and the meridian sun strikes the
                    upper surface of the impenetrable foliage of
                    my trees.While the lovely valley teems with
                    vapour around me.</p>
            </div>
            <div class="col-12 col-sm-6 col-lg-3">
                <h3 class="text-uppercase fw-bold">Quick links</h3>
                <Divider/>
                <ul class="list-unstyled">
                    <li v-for="link in links" class="mb-1">
                        <a href="#">{{ link.text }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-12 col-sm-6 col-lg-3">
                <h3 class="text-uppercase fw-bold">contact</h3>
                <Divider/>
                <ul class="list-unstyled">
                    <li v-for="contact in contacts" class="mb-4">
                        <a href="#">{{ contact.text }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-12 col-sm-6 col-lg-3">
                <h3 class="text-uppercase fw-bold">location on map</h3>
                <Divider/>
                <img src="/images/map.png" alt="map" class="img-fluid">
            </div>
        </div>
        <EndBar/>
    </footer>
</template>

<script>
import { links } from '../data/data';
import { contacts } from '../data/data';
import Divider from './Divider.vue';
import EndBar from './EndBar.vue'
    export default {
    name: 'FooterComponent',
    components: {
            Divider, EndBar
    },
    data() {
        return {
            links,
            contacts
        }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
a{
    text-decoration: none;
    color: black;
    transition: .2s;
    &:hover{
        color: $contrast-color;
        text-decoration: underline;
    }
}
</style>