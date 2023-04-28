<template>
    <section class="m-5 py-5">
        <div class="row justify-content-center align-items-center">
            <div class="col-12 col-md-4 col-lg-2 d-flex justify-content-center align-items-center py-3" v-for="sponsor in sponsors">
                <img :src="sponsor.image" :alt="sponsor.name" class="img-fluid h-50">
            </div>
        </div>
    </section>
</template>

<script>
import {sponsors} from '../data/data'
    export default {
    name: 'Sponsors',
    data() {
        return {
                sponsors
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
.row{
    height: 110px;
    overflow-y: auto;
    min-height: 300px;
    .col-12{
        height: 100%;
        transition: .5s;
        &:hover{
            background: $text-grey;
            cursor: pointer;
        }
        border-radius: 20px;
    }
}

</style>