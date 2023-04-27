<script>
import NavMenu from '../data/NavMenu'
import IconSocial from '../data/IconSocial'
export default {
    name: 'NavFooter',
    data() {
        return {
            dataNavMenu: NavMenu,
            dataIconSocial: IconSocial
        }
    },
}
</script>
<template>
    <nav class="d-flex justify-content-between align-items-baseline">
        <div class="navbar-brand">
            <img src="../assets/img/logotype-2-300x50.png" alt="">
        </div>
        <ul class="navbar-item d-flex py-3">
            <li v-for="menu in dataNavMenu" class="p-2">
                <a :href=" '#' + menu.title.toUpperCase()">{{ menu.title.toUpperCase() }}</a>
            </li>
        </ul>
        <div class="nav-link ">
            <a class="p-2" href="icon.link" v-for="icon in dataIconSocial" v-html="icon.svg"></a>
        </div>
    </nav>
</template>