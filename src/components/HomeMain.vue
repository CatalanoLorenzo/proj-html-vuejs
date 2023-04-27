<script>
import AboutMenu from '../data/AboutMenu'
export default{
    name:'HomeMain',
    data() {
        return {
            dataAboutMenu: AboutMenu,
        }
    },
}
</script>
<template>
    <section class="home position-relative py-5 " id="HOME">
        <div class="decoration_line position-absolute"></div>
        <div class="container py-5 px-5">
            <div class="d-flex align-center px-5 mx-5">
                <h3 class="py-5 my-5 "><strong>OUR CONSULTANTS CAN HELP YOU</strong></h3>
            </div>
            <div class="row row-cols-2 g-2 px-5  mx-5">
                <!-- element for about dinamic  -->
                <div class="col d-flex align-items-start p-0 m-0" v-for="badge in dataAboutMenu">
                    <div class="circle  mx-3" v-html="badge.icon">
                    </div>
                    <div class="text_area p-3">
                        <h4 class=""><strong>{{ badge.title.toUpperCase() }}</strong></h4>
                        <p class=" fs-6">{{ badge.description }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>