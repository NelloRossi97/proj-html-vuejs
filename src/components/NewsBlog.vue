<template>
    <section class="my-5 mx-2 d-flex flex-column justify-content-center">
        <div class="d-flex flex-column align-items-center">
            <h2 class="fs-1 fw-bold">Latest News & Our <span>Blog</span></h2>
            <Divider/>
        </div>

        <div class="row">
            <div class="col-12 my-card position-relative d-flex justify-content-center" v-for="item in news">
                <img :src="item.image" :alt="item.title" class="img-fluid rounded-4">
                <div id="info" class="position-absolute p-4">
                    <p>{{ item.date }} by {{ item.creator }}</p>
                    <div class="d-flex align-items-center">
                        <i class="fa-solid fa-circle me-2"></i> 
                        <h2>{{ item.title }}</h2>
                    </div>
                    
                </div>
            </div>
        </div>

        <div class="button-container d-flex justify-content-center">
            <ButtonSecondary :text="'view all posts'"/>
        </div>
        
    </section>
</template>

<script>
import {news} from '../data/data'
import Divider from './Divider.vue';
import ButtonSecondary from './ButtonSecondary.vue'
    export default {
    name: 'NewsBlog',
    components: { Divider, ButtonSecondary },
    data() {
        return {
                news
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
section{
    height: 100vh;
}
h2{
    
    span{
        color: $contrast-color;
    }
}
.row{
    transition: 1s;
}
.my-card{
    width: 33%;
    transition: 1s;
    &:hover{
        z-index: 100;
        img{
            scale: 1.1;
        }
        cursor: pointer;
        #info{
            background: $hover-bg-reverse;
            bottom: -7rem;
            i{
                color: $text-grey;
            }
        }
    }
    #info{
        bottom: -5rem;
        background: white;
        border-radius: 5px;
        box-shadow: 0 4px 0 rgba(34,34,34,.03);
        width: 80%;
        transition: 1s;
        i{
            font-size: 0.8rem;
            color: $contrast-color;
        }
        p{
            font-size: 0.9rem;
            color:$text-grey;
        }
    }
}
.button-container{
    margin-top: 10rem;
}
</style>