<script>
import AboutMenu from '../data/AboutMenu'
export default {
    name: 'PageMain',
    data() {
        return {
            dataAboutMenu: AboutMenu,
        }
    },
}
</script>
<template>
    <main>
        <section class="home position-relative py-5 ">
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
        <section class="about">
            <div class="top">
                <div class="container-fluid mx-0 px-0">
                    <div class="row">
                        <div class="col-6 px-0">
                            <div class="teams_img">
                                <img class="w-100"
                                    src="../assets/img/business-people-working-together-on-project-and-5FHSKBL-1390.jpg"
                                    alt="">

                            </div>
                        </div>
                        <div class="col align-items-center d-flex">
                            <div class="text_area overflow-hidden px-5 col-5">
                                <div class="b_title d-flex align-items-center">
                                    <div class="decoration_line"></div>
                                    <span class="p-3"><strong>ABOUT US</strong></span>
                                </div>
                                <h1><strong>WE MAKE YOUR STRATEGY WORK</strong></h1>
                                <p class="py-3">
                                    When,while lovely calley teems with vapour around meand eridian sun strikes the upper
                                    impenetrable foliage of my trees,and but a thousand unknown plants are noticed when I
                                    hear the buzz of the little worls among the stalks,and grow familiar indescribable forms
                                    of the insects .and flies, then I feel the presence of the Almighty.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="bottom py-5 position-relative">
                <div class="container">
                    <div class="row gap-5">
                        <div class="col-3 py-5 px-4 mx-5">
                            <h4 class="">
                                <strong>
                                    WE HELP TO DELIVER  THE  BUSINESS CASE
                                </strong>

                            </h4>
                        </div>
                        <div class="col-4 py-5 px-4">
                            <p>
                                When,while lovely calley teems with vapour around meand eridian sun strikes the upper
                                impenetrable foliage of my trees,and but a thousand unknown
                            </p>
                        </div>
                    </div>
                </div>
                <button class=" position-absolute border-0 p-3">GET STARTED</button>
            </div>
        </section>
        <section class="projects"></section>
        <section class="services"></section>
        <section class="blog"></section>
    </main>
</template>