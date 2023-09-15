<script setup>
    import { Link } from '@inertiajs/vue3';

    import { defineProps } from 'vue';
    defineProps({
    collapse:Boolean
  })


</script>

<template>

<div class="main-nav" :class="collapse">
    <Link href="#">
        <i class="fa fa-home"></i>
         <span v-show="!collapse">Home</span> 
    </Link>
    <Link href="#">
        <i class="fa fa-question"></i>
        <span v-show="!collapse" >About Us</span> 
    </Link>
    <Link href="#">
        <i class="fa-solid fa-cart-shopping"></i> 
        <span v-show="!collapse" >Products</span>
    </Link>
    <Link href="#">
        <i class="fa-regular fa-images"></i> 
        <span v-show="!collapse" >Gallery</span>
    </Link>
    <Link href="#">
        <i class="fa-solid fa-phone-volume"></i> 
        <span v-show="!collapse" >Contact Us</span>
    </Link>
</div>

</template>
<style>
    .visible {
        width: 350px!important;
    }

    .close {
        width: 60px!important;
    }
</style>