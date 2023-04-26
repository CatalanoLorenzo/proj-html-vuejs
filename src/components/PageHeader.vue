
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
        <!-- nav bar -->
        <nav class="navbar position-fixed  w-100">
            <div class="container ">

                <!-- logo -->
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logotype.png" alt="Bootstrap" width="30" height="24">
                </a>

                <!-- link nav menu -->
                <ul class="navbar-nav d-flex flex-row">
                    <li class="nav-item px-3 py-2" v-for="li in dataNavMenu">
                        <a class="nav-link " :href="li.toUpperCase()">{{ li.toUpperCase() }}</a>
                    </li>
                </ul>

            </div>
        </nav>

        <section class="jumbo ">
            <div class="container d-flex align-items-center">
                <div class="row flex-column justify-content-center">
                    <div class="col-4 ">
                        <!-- intro text -->
                        <div class=" d-flex align-items-baseline ">
                            <div class="decoration_line"></div><span class="b_title px-3 py-2">ALWATS THE BEST WAY YOU NEED
                                IT</span>
                        </div>
                        <!-- h1 -->
                        <div class="">
                            <h1 class="">THE BEST BUSINESS CONSULTING</h1>
                        </div>
                        <!-- button -->
                        <div class="">
                            <button class="">Read More</button>
                            <div class="play_icon"></div>
                        </div>
                    </div>

                </div>
            </div>

        </section>

    </header>
</template>
