<script setup>
import {ref,inject} from 'vue'
const data=inject('mydata')
const msg=inject('message')
import { ydata } from '../data/ydata';
</script>
<template>
    <h2 class="my-5"> Child Component</h2>
    <p class="my-10 text-orange-500">
        {{ data.mesasge }} | {{ data.count }}
    </p>
   <P class="my-5">
    {{ msg }}
   </P>
    <p>
        <button @click="data.increase()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                 +++
        </button>
        <button @click="data.decrease()" class="mx-10 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                ---
        </button>
    </p>
    
</template>
<style scoped></style>