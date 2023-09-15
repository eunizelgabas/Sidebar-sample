<script setup>
    import MainNav from '@/Components/MainNav.vue'
    import { ref } from 'vue';

    let width = ref('w-[250px]')
    let hidden = ref("")
    let isCollapsed = ref(false)

    function toggleWidth() {
        if(width.value == 'w-[250px]') {
            width.value = 'w-[100px]'
            hidden.value = "hidden"
            isCollapsed.value =!isCollapsed.value

        }else {
            width.value = ['w-[250px]']
            hidden.value = ""
            isCollapsed.value =!isCollapsed.value

        }
    }

    const props = defineProps({
        openSidebar: Boolean
    })
</script>

<template>

<div class="flex min-h-screen">
    <div id="sidebar" class="bg-blue-900 p-6 duration-500" :class="width" style="position: relative;">
        <button class="text-xl text-tahiti" @click="toggleWidth" style="position: absolute; right: 10px; top:10px">
            <i class="fa-solid fa-bars"></i>
        </button>
        <div id="branding" :class="hidden">
            <img src="https://t3.ftcdn.net/jpg/05/99/02/82/360_F_599028203_2VGmVRpAzzrlqw5HWqbe5FOrhkPWzYzt.jpg" alt="Logo"
                class="w-[170px] h-[170px] mx-auto rounded-full object-cover">
            <h1 class="text-3xl text-center text-yellow-400 my-6">IDK Homes</h1>

        </div>
        

        <MainNav :collapse="isCollapsed"/>
    </div>
    <div id="container" class="flex-1 ">
        <slot />
    </div>
</div>

</template>