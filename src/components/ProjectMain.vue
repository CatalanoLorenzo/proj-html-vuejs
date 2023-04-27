<script>
import ImgCarousel from '../data/imgcarousel'
export default {
    name: 'ProjectMain',
    data() {
        return {
            dataImgCarousel: ImgCarousel,
        }
    },
}
</script>
<template>
    <section class="projects p-5 m-0">
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
                            <button class="button_left border-0 p-3 m-1">
                                <svg xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                    <path
                                        d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l128 128c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.3 288 480 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-370.7 0 73.4-73.4c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-128 128z" />
                                </svg>
                            </button>
                            <button class="button_right border-0 p-3 m-1">
                                <svg xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                    <path
                                        d="M502.6 278.6c12.5-12.5 12.5-32.8 0-45.3l-128-128c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L402.7 224 32 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l370.7 0-73.4 73.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l128-128z" />
                                </svg>
                            </button>
                        </div>

                    </div>
                    <div class="carousel">
                        <div class="container">
                            <div class="row row-cols-3">
                                <div class="col py-2" v-for="img in dataImgCarousel">
                                    <img :src="img.url" :alt="img.title">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>


    </section>
</template>