<script>
import NavFooter from './NavFooter.vue';
export default {
    name: 'BottomFooter',
    props:{
        arrayMenu:Array
    },
    components:{
        NavFooter
    }
}
</script>
<template>
    <div class="bottom py-5 px-5 mx-5">
        <NavFooter  :arrayMenu="arrayMenu"></NavFooter>
        <hr class="px-5">
        <div class=" w-100">
            <div class="row justify-content-between ">
                <div class="col">
                    <p>Terms of use</p>
                    <p>Privacy Environmental Policy</p>
                </div>
                <div class="col text-end">
                    <p>Copyright © 2020 Phloc Consulting.All Rights Reserved</p>
                </div>
            </div>
        </div>
    </div>
</template>