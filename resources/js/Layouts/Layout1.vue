<script setup>
    import MainNav from '@/Components/MainNav.vue'
    import { useForm } from '@inertiajs/vue3';
    import { watch } from 'vue';
    import { ref, provide  } from 'vue';

    let width = ref('w-[250px]')
    let hidden = ref("")
    let isCollapsed = ref(false)

    const motif = ref("bg-purple-500")
    
    function changeColor(color){
       motif.value = color
    }
    
    provide('the_motifs', motif)

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
        openSidebar: Boolean,
        motif: String,
    })
</script>

<template>

<div class="flex min-h-screen">
    <div id="sidebar" class="p-6 duration-500" :class="[motif, width]" style="position: relative;">
        <button class="text-xl text-tahiti" @click="toggleWidth" style="position: absolute; right: 10px; top:10px">
            <i class="fa-solid fa-bars"></i>
        </button>
        <div id="branding" :class="hidden">
            <img src="https://t3.ftcdn.net/jpg/05/99/02/82/360_F_599028203_2VGmVRpAzzrlqw5HWqbe5FOrhkPWzYzt.jpg" alt="Logo"
                class="w-[170px] h-[170px] mx-auto rounded-full object-cover">
            <h1 class="text-3xl text-center text-yellow-400 my-6">IDK Homes</h1>

        </div>
        

        <MainNav :collapse="isCollapsed"/>

        <!-- <select @click="changeColor" v-model="motif" class="mt-5 py-3 px-4 pr-9 block w-full border-gray-200 rounded-md text-sm focus:border-blue-500 focus:ring-blue-500 dark:bg-slate-900 dark:border-gray-700 dark:text-gray-400">
            <option selected disabled>Open this select menu</option>
            <option value="red">Red</option>
            <option value="blue">Blue</option>
            <option value="green">Green</option>
        </select> -->
        <div class="flex justify-center space-x-2 mt-5">
         <button @click="changeColor('bg-blue-900')" class="inline-flex items-center px-5 py-5 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"> </button>
         <button @click="changeColor('bg-red-900')" class="inline-flex items-center px-5 py-5 text-sm font-medium text-center text-white bg-red-700 rounded-lg hover:bg-red-800 focus:ring-4 focus:outline-none focus:ring-red-300 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-800"> </button>
         <button @click="changeColor('bg-green-900')" class="inline-flex items-center px-5 py-5 text-sm font-medium text-center text-white bg-green-700 rounded-lg hover:bg-green-800 focus:ring-4 focus:outline-none focus:ring-green-300 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800"> </button>
        </div>
    </div>
    <div id="container" class="flex-1 ">
        <slot />
    </div>
</div>

</template>