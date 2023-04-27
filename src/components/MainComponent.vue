<template>
    <main>
        <Jumbotron/>
        <Services/>
        <LearnAbout/>
        <Showcase/>
    </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import Services from './Services.vue';
import LearnAbout from './LearnAbout.vue';
import Showcase from './Showcase.vue';
    export default {
    name: 'MainComponent',
    components: {
        Jumbotron,
        Services,
        LearnAbout,
        Showcase
        }
    }
</script>

<style lang="scss" scoped>

</style>