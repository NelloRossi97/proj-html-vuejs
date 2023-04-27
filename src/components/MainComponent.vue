<template>
    <main>
        <Jumbotron/>
        <Services/>
        <LearnAbout/>
    </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import Services from './Services.vue';
import LearnAbout from './LearnAbout.vue';
    export default {
    name: 'MainComponent',
    components: {
        Jumbotron,
        Services,
        LearnAbout
        }
    }
</script>

<style lang="scss" scoped>

</style>