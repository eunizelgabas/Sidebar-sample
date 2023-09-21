<script setup>
    import Layout1 from '@/Layouts/Layout1.vue'
    import Card2 from '@/Components/Card2.vue'
    import { computed, inject, ref } from 'vue';

    const props = defineProps({
        motif : String,
    })

   
    // const motifs = inject('the_motifs')

    // // const selectedMotifClass = ref(motif);
    // const motifClass = computed(() => motifs.value)
   
</script>

<template>

<Layout1>
    <nav class="flex items-center justify-between p-2 bg-gray-300">
        <h1 class="text-4xl">Home</h1>
    </nav>
    <div class="p-8 mt-5">
       <h5>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus sodales felis pellentesque, posuere nulla ac, vehicula turpis. Aenean sed lorem dictum, pharetra nunc eget, vehicula sem. Maecenas tincidunt vitae eros eu scelerisque. Donec sodales felis et mi vulputate, nec placerat mi pulvinar. Quisque blandit tellus ac diam consectetur, in consectetur neque lacinia. Sed pretium tincidunt lacus, vel pharetra magna sollicitudin quis. Nunc tellus erat, ullamcorper rhoncus justo eget, egestas convallis diam. Curabitur a augue sed diam pharetra efficitur et non quam. Suspendisse quis faucibus tellus, ac imperdiet dolor. Vivamus at aliquam risus. Donec viverra, ipsum a lacinia lobortis, mauris nisi laoreet turpis, et vulputate quam quam quis nisi. Aenean quis risus tortor. </h5>
        <p class="text-center">
            Proin tempus nulla sit amet rhoncus aliquam. Morbi dictum augue id dapibus dapibus. Nullam auctor, dui nec ultricies pulvinar, arcu dolor euismod arcu, quis condimentum mi mauris finibus dolor. Donec ante felis, dignissim non nunc eget, porta tempus nunc. Sed a nunc rutrum, tempor ipsum non, congue sem. Aliquam id sapien sollicitudin, lacinia est quis, fringilla justo. Sed dignissim, tellus pretium scelerisque luctus, arcu turpis mattis ex, id dignissim nisi sem a nulla. Interdum et malesuada fames ac ante ipsum primis in faucibus. Integer eu pulvinar ex. Proin sed erat cursus diam cursus vulputate. In posuere massa ante, quis mattis lacus dignissim ut. Sed nec vulputate ex. 
        </p>
        <Card2/>
        <!-- <button :class="motifClass" class="items-center px-3 py-3 text-sm font-medium text-center text-white bg-green-700 rounded-lg hover:bg-green-800 focus:ring-4 focus:outline-none focus:ring-green-300 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800"> Get Started</button> -->
    </div>
</Layout1>

</template>

