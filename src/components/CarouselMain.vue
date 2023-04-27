<script>
export default {
    name: 'CarouselMain',
    props:{
        array:Array
    },
    data() {
        return {
            
        }
    },
}
</script>
<template>
    <div class="carousel">
        <div class="container">
            <div class="row row-cols-3">
                <div class="col py-2 position-relative" v-for="img in array" v-show="img.visible">
                    <img :src="img.url" :alt="img.alt">
                    <div class="info position-absolute d-flex justify-content-between w-100" v-show="true">
                        <div class="text mx-3">
                            <h4>{{ img.title }}</h4>
                            <p>{{ img.category }}</p>
                        </div>
                        <button class="border-0 mx-5">
                            <svg xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 448 512"><!--! Font Awesome Pro 6.4.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
                                <path
                                    d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32V224H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H192V432c0 17.7 14.3 32 32 32s32-14.3 32-32V288H400c17.7 0 32-14.3 32-32s-14.3-32-32-32H256V80z" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>