<script>
import ServiceBages from '../data/ServiceBages'
export default {
    name: 'ServiceMain',
    data() {
        return {
            dataServiceBages: ServiceBages,
        }
    },
}
</script>
<template>
    <section class="services" id="SERVICES">
        <div class="container-fluid m-auto">
            <div class="row flex-column  ">
                <div class="col align-items-end flex-column d-flex">
                    <div class="b_title d-flex align-items-center justify-content-between py-5">
                        <span class="px-3">TESTIMONIAL</span>
                        <div class="decoration_line"></div>
                    </div>
                    <h2 class=" text-end">WHAT'S THE CUSTOMER SAY ABOUT OUR WORK</h2>
                </div>

            </div>
        </div>
        <div class="container show_badges d-flex justify-content-end">
            <div class="row p-5 ">
                <div class="col  gap-5 d-flex p-2">
                    <div class="bage p-2" v-for="badge in dataServiceBages">
                        <p class="text">{{ badge.text }}</p>
                        <h4>{{ badge.title }}</h4>
                        <p>{{ badge.subTitle }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>