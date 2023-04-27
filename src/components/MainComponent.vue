<template>
    <main>
        <Jumbotron/>
        <Services/>
    </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import Services from './Services.vue';
    export default {
    name: 'MainComponent',
    components: {
        Jumbotron,
        Services
        }
    }
</script>

<style lang="scss" scoped>

</style>