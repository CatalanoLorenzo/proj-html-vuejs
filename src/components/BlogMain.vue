<script>
import BlogPosts from '../data/BlogPosts'
export default{
    name:'BlogMain',
    data() {
        return {
            dataBlogPosts: BlogPosts
        }
    },
}
</script>
<template>
    <section class="blog" id="BLOG">
        <div class="container position-relative py-5">
            <div class="row flex-column">
                <div class="col position-relative py-3">
                    <div class="b_title d-flex align-items-center  py-5">
                        <div class="decoration_line"></div>
                        <span class="px-3">BLOG</span>
                    </div>
                    <h2><strong>THE RECENT NEWS YOU MUST READ IT</strong></h2>
                    <button class="border-0 position-absolute">VIEW ALL</button>
                </div>
                <div class="col d-flex gap-5 py-5">
                    <div class="post position-relative" v-for="post in dataBlogPosts">
                        <img :src="post.url" alt="post.title">
                        <div class="info position-absolute p-5">
                            <span class="px-5 py-2"><strong>{{ post.data }}</strong></span><span><strong>by
                                    {{ post.autor }}</strong></span>
                            <h3 class="px-5 py-2">{{ post.title }}</h3>
                            <p class="px-5">{{ post.text }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>