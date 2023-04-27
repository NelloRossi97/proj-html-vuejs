<template>
    <main>
        <Jumbotron/>
        <Services/>
        <LearnAbout/>
        <Showcase/>
        <Comment/>
    </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import Services from './Services.vue';
import LearnAbout from './LearnAbout.vue';
import Showcase from './Showcase.vue';
import Comment from './Comment.vue';
    export default {
    name: 'MainComponent',
    components: {
        Jumbotron,
        Services,
        LearnAbout,
        Showcase,
        Comment
        }
    }
</script>

<style lang="scss" scoped>

</style>