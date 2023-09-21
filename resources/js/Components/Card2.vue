<script setup>
import { computed } from 'vue';
import { inject, ref } from 'vue';


const motif = inject('the_motifs')

const motifClass = computed(() => motif.value);

</script>

<template>

    <!-- <div class="card">
        <h1>"I am a second child"</h1>
    </div> -->

      <button href="#" :class="motifClass" class="rounded-sm inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white ">
        Get Started 
        <svg class="w-3.5 h-3.5 ml-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
        </svg>
    </button>
    <!-- <p :class="motifClass" type="button" class=" inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white " >This text has the injected color class.</p> -->

</template>