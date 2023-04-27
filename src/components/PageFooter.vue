<script>
import TopFooter from './TopFooter.vue'
import BottomFooter from './BottomFooter.vue'
export default {
    name: 'PageFooter',
    components: {
        TopFooter,
        BottomFooter
    },
}
</script>
<template>
    <footer>
        <TopFooter></TopFooter>
        <BottomFooter></BottomFooter>
    </footer>
</template>