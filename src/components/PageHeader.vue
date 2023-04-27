
<script>
import NavHeader from './NavHeader.vue';
import JumboHeader from './JumboHeader.vue'
export default {
    name: 'PageHeader',
    components:{
        NavHeader,
        JumboHeader,
    },
}
</script>
<template>
    <header>
        <NavHeader></NavHeader>
        <JumboHeader></JumboHeader>
    </header>
</template>
