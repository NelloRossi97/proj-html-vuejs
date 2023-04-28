<template>
    <main>
        <Jumbotron/>
        <Services/>
        <LearnAbout/>
        <Showcase/>
        <Comment/>
        <NewsBlog/>
        <CallToAction/>
        <Sponsors/>
    </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import Services from './Services.vue';
import LearnAbout from './LearnAbout.vue';
import Showcase from './Showcase.vue';
import Comment from './Comment.vue';
import NewsBlog from './NewsBlog.vue';
import CallToAction from './CallToAction.vue';
import Sponsors from './Sponsors.vue';
    export default {
    name: 'MainComponent',
    components: {
        Jumbotron,
        Services,
        LearnAbout,
        Showcase,
        Comment,
        NewsBlog,
        CallToAction,
        Sponsors
        }
    }
</script>

<style lang="scss" scoped>

</style>