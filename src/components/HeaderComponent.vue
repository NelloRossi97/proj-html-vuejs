<template>
    <header>
        <TopBar/>
        <NavBar/>
    </header>
</template>

<script>
import TopBar from './TopBar.vue';
import NavBar from './NavBar.vue';
    export default {
    name: 'HeaderComponent',
    components: {
        TopBar,
            NavBar
        }
    }
</script>

<style lang="scss" scoped>

</style>