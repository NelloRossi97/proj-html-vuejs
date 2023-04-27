<template>
    <div class="col-12 p-5">
        <i :class="'fa-solid fa-' + icon + ' fs-1'"></i>
        <h3 class="text-capitalize my-4">{{ title }}</h3>
        <p>Far far away, behind the word mountains, far
            from the countries Vokalia Separated...</p>
    </div>
</template>

<script>
    export default {
    name: 'Card',
    props: ['icon', 'title']
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
.left{
    width: 40%;
}

.right{
    max-width: 60%;
}

.col-12{
    box-shadow: 0 4px 44px 0 rgba(0, 0, 0, 0.14);
    border-radius: 20px;
    max-width: 450px;
    max-height: 400px;
    &:hover{
        color: white;
        background: $hover-bg;
        box-shadow: 6px 6px 25px 0 rgba(0,217,166,.35);
        cursor: pointer;
    }
}
</style>