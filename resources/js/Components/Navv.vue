<script setup>
import { computed } from 'vue';
import { inject } from 'vue';

     const motif = inject('the_motifs')

    // const selectedMotifClass = ref(motif);
    const motifClass = computed(() => motif.value)
</script>

<template>
    <div class="border-4 duration-500" :class="motifClass" >
        <nav class="flex items-center justify-between p-2">
        <h1 class="text-4xl">Home</h1>
    </nav>
    </div>
   
</template>