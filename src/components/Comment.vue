<template>
    <section class="my-5">
        <div class="comment-container w-100 h-100 d-flex flex-column justify-content-center align-items-center text-white text-center">
            <i class="fa-solid fa-quote-left"></i>
            <p class="my-5 fs-4">When it comes to barbequing, there are two main schools of
                thought for the techniques that you can use. Freshly scrambled
                eggs with applewood smoked bacon - are amazing!</p>
            <img src="/images/lissa-durbin.jpg" alt="Lissa durbin" class="my-4">
            <h4 class="text-uppercase">lissa durbin</h4>
            <span>Client</span>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'Comment'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
section{
    height: 100vh;
    background-image: url('/images/meeting.jpg');
    background-size: cover;
    .comment-container{
        background: rgba(29, 29, 29, 0.9);
        z-index: 100;
        i{
            color: $contrast-color;
            font-size: 4rem;
        }
        p{
            font-style: italic;
            max-width: 60%;
        }
        img{
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 5px solid white;
        }
        h4{
            color: $contrast-color;
        }
    }
}
</style>