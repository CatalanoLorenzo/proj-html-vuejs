<script>
import NavMenu from '../data/NavMenu'
export default {
    name: 'NavHeader',
    data() {
        return {
            dataNavMenu: NavMenu
        }
    },
    methods: {
        chageSelect(position) {

            for (let i = 0; i < this.dataNavMenu.length; i++) {
                const element = this.dataNavMenu[i];
                if (element.select) {
                    element.select = false
                }
            }
            this.dataNavMenu[position - 1].select = true
        }
    },
}
</script>
<template>
    <!-- nav bar -->
    <nav class="navbar position-fixed  w-100">
        <div class="container ">
            <!-- logo -->
            <a class="navbar-brand" href="#">
                <img src="../assets/img/logotype.png" alt="Bootstrap" width="30" height="24">
            </a>
            <!-- link nav menu -->
            <ul class="navbar-nav d-flex flex-row">
                <li class="nav-item px-3 py-2" v-for="li in dataNavMenu" :class="li.select ? 'select' : ''">
                    <a class="nav-link " :href="'#' + li.title.toUpperCase()" :value="li.position" @click="chageSelect(li.position)">{{ li.title.toUpperCase() }}</a>
                </li>
            </ul>

        </div>
    </nav>
</template>