<script setup>
import {ref,reactive} from 'vue'
const favColors= ref([])
</script>

<template >
<section class="mx-auto container">
    <h1 class="text-2xl mb-10"> Vue Form</h1>
    <p class="mb-5">{{ favColors }}</p>
    Your favorite colors <br>
    <label for="red"> Red</label>
    <input class="ml-2 mr-2" type="checkbox" id="red" v-model="favColors" value="red"/>
    <label for="blue"> Green</label>
    <input class="ml-2 mr-2" type="checkbox" id="green" v-model="favColors" value="green"/>
    <label for="blue"> Blue</label>
    <input class="ml-2 mr-2" type="checkbox" id="blue" v-model="favColors" value="blue"/>
    
    <!-- <img
    v-show="displayImage"
    class="mt-10 mx-auto w-[500px]"
    :src="`https://source.unsplash.com/random?version=${Math.random()}`"
    alt=""
    /> -->
    
</section>



</template>

<style scoped>


</style>
