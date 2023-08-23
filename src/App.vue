<script setup>
import {ref,reactive,provide} from 'vue'
import ParentComponent from './components/ParentComponent.vue';
import { ydata } from './data/ydata';

const msg=ref('hello World')
const data=reactive({
    mesasge:"Hello World",
    count:1,
    increase(){
        this.count++
    },
    decrease(){
        this.count--
    }
})
provide('mydata',data) // register data to be availabe to all child Component
provide('message',msg)
</script>
<template>
    <p class="text-2xl font-bold my-10"> Prop Driling</p>
    <p class="text-red-500 my-10">
        {{ data.mesasge }} | {{ data.count }}
    </p>
    <p class="text-red-500 my-10">
        Ydata {{ ydata.mesasge }} | {{ ydata.count }}
    </p>
  <ParentComponent/>
  
</template>
<style scoped>
</style>