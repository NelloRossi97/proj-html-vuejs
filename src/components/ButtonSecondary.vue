<template>
    <button class="button-primary">{{ text }}</button>
</template>

<script>
export default {
    name: 'ButtonSecondary',
    props: ['text']
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

button {
    background: $gradient-secondary;
    border-radius: 50px;
    color: white;
    text-transform: uppercase;
    padding: 20px 45px;
    font-size: 0.8rem;
    border: none;
    &:hover {
        background: $gradient-primary;
        box-shadow: 6px 6px 25px 0 rgba(0, 217, 166, .35);
    }
}
</style>