<script setup>
import { ydata } from '../data/ydata';
import {ref,inject} from 'vue'
// const data=inject('mydata')
// const msg=inject('message')
</script>
<template>
    <h2 class="my-5"> Child X Component</h2>
    
   <P class="my-5">
    {{ msg }}
   </P>
    <p>
        <button @click="ydata.increase()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                 ++
        </button>
        <button @click="ydata.decrease()" class="mx-10 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                --
        </button>
    </p>
    
</template>
<style scoped></style>