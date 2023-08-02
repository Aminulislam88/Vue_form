<script setup>
import {ref,reactive} from 'vue'
const saarcCountries=reactive([
    {name:"Bangladesh",capital:"Dhaka"},
    {name:"Nepal", capital:"Kathmandu"},
    {name:"Bhutan", capital:"Thimpu"},
    {name:"Srilanka",capital:"Colombo"},
    {name:"India",capital:"Delhi"},
    {name:"Maldives",capital:"Male"},
    {name:"Pakistan",capital:"Islamabad"}
])
const capitals=["Dhaka","Kathmandu","Thimpu","Colombo","Delhi","Male","Islamabad"]

function getScore(){
    let score=0;
    saarcCountries.forEach(country=>{
        if(country.capital==country.answer)
        score++
    })
    return score

}

// function getRandomCapitals(){

//   return capitals.sort(()=>Math.random() - 0.5)
// }
</script>


<template >
<section class="mx-auto container">
    <h1 class="text-2xl mb-10"> Vue Form</h1>
    <p class="mb-5">{{ saarcCountries }}</p>
    <p>Your score: {{ getScore() }} </p>
    <div class="my-5 border border-gray-400 p-5" v-for="(country,index) in saarcCountries" :key="country.name">
        <p>What is the capital of {{ country.name }} ?</p>
        <template v-for="capital in capitals">
        <input :name="country.name" type="radio" :value="capital" v-model="country.answer"/>
        <label class="ml-2 mr-2">{{ capital }}</label>
        </template>
    </div>
   
    
</section>



</template>

<style scoped>


</style>
