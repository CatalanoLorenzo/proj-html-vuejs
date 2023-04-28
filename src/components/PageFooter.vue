<script>
import TopFooter from './TopFooter.vue'
import BottomFooter from './BottomFooter.vue'
import NavMenu from '../data/NavMenu'
export default {
    name: 'PageFooter',
    components: {
        TopFooter,
        BottomFooter,
        NavMenu
    },
    data() {
        return {
            dataNavMenu: NavMenu
        }
    },
}
</script>
<template>
    <footer>
        <TopFooter></TopFooter>
        <BottomFooter :arrayMenu="dataNavMenu"></BottomFooter>
    </footer>
</template>