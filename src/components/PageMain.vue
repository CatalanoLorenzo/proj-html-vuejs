<script>
import HomeMain from './HomeMain.vue';
import AboutMain from './AboutMain.vue'
import ProjectMain from './ProjectMain.vue'
import ServiceMain from './ServiceMain.vue'
import BlogMain from './BlogMain.vue'
export default {
    name: 'PageMain',
    components:{
        HomeMain,
        AboutMain,
        ServiceMain,
        ProjectMain,
        BlogMain
    },
}
</script>
<template>
    <main>
        <HomeMain></HomeMain>
        <AboutMain></AboutMain>
        <ProjectMain></ProjectMain>
        <ServiceMain></ServiceMain>
        <BlogMain></BlogMain>
    </main>
</template>