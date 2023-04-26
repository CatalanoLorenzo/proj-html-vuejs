
<script>
import NavMenu from '../data/NavMenu'
export default {
    name: 'PageHeader',
    data() {
        return {
            dataNavMenu: NavMenu
        }
    },
}
</script>
<template>
    <header>
        <nav class="navbar position-fixed  w-100">
            <div class="container ">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logotype.png" alt="Bootstrap" width="30" height="24">
                </a>

                <ul class="navbar-nav d-flex  ">
                    <li class="nav-item" v-for="li in dataNavMenu">
                        <a class="nav-link active" :href="li.toUpperCase()">{{ li.toUpperCase() }}</a>
                    </li>
                    
                </ul>

            </div>
        </nav>

    </header>
</template>
