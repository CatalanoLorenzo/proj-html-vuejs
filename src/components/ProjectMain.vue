<script>
import CarouselMain from './CarouselMain.vue';
import ImgCarousel from '../data/imgcarousel'

export default {
    name: 'ProjectMain',
    components: {
        CarouselMain,
    },
    data() {
        return {
            dataImgCarousel: ImgCarousel,
            counter: 0
        }
    },
    methods: {
        chageVisibleMore() {
            if ((this.counter ) == this.dataImgCarousel.length - 3) {
                this.dataImgCarousel[this.counter].visible = false
                this.dataImgCarousel[0].visible = true
                this.counter++
            }else if ((this.counter ) == this.dataImgCarousel.length - 2){
                this.dataImgCarousel[this.counter].visible = false
                this.dataImgCarousel[1].visible = true
                this.counter++
            }else if ((this.counter ) == this.dataImgCarousel.length - 1){
                this.dataImgCarousel[this.counter].visible = false
                this.dataImgCarousel[2].visible = true
                this.counter = 0
                   
            }else{
                this.dataImgCarousel[this.counter + 3].visible = true
                this.dataImgCarousel[this.counter].visible = false
                this.counter++
            }
        },
        chageVisibleLess() {
            if ((this.counter ) == 2) {
                this.dataImgCarousel[this.counter].visible = false
                this.dataImgCarousel[this.dataImgCarousel.length - 1].visible = true
                this.counter--
            }else if ((this.counter ) == 1){
                this.dataImgCarousel[this.counter].visible = false
                this.dataImgCarousel[this.dataImgCarousel.length - 2].visible = true
                this.counter--
            }else if (this.counter  == 0){
                this.dataImgCarousel[this.counter].visible = false
                this.dataImgCarousel[this.dataImgCarousel.length - 3].visible = true
                this.counter = this.dataImgCarousel.length - 1
                   
            }else{
                this.dataImgCarousel[this.counter ].visible = false
                this.dataImgCarousel[this.counter - 3].visible = true
                this.counter--
            }
        }

    }
}
</script>
<template>
    <section class="projects p-5 m-0" id="PROJECTS">
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="b_title d-flex align-items-center py-5">
                        <div class="decoration_line"></div>
                        <span class="px-3">PROJECT</span>
                    </div>
                    <div class="title d-flex justify-content-between">
                        <span class="fs-1"><strong>OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS</strong></span>
                        <div class="button">
                            <button class="button_left border-0 p-3 m-1" @click="chageVisibleLess()">
                                <svg xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                    <path
                                        d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l128 128c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.3 288 480 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-370.7 0 73.4-73.4c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-128 128z" />
                                </svg>
                            </button>
                            <button class="button_right border-0 p-3 m-1 " @click="chageVisibleMore()">
                                <svg xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                    <path
                                        d="M502.6 278.6c12.5-12.5 12.5-32.8 0-45.3l-128-128c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L402.7 224 32 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l370.7 0-73.4 73.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l128-128z" />
                                </svg>
                            </button>
                        </div>

                    </div>
                    <CarouselMain :array="dataImgCarousel"></CarouselMain>
                </div>
            </div>
        </div>


    </section>
</template>