<script setup>
import{ ref,inject} from 'vue'
import ChildComponent from './ChildComponent.vue';
import ChildComponentX from './ChildComponentX.vue';
const data=inject('mydata')
</script>
<template>
    <h2> Parant Component</h2>
    <p class="my-10 text-green-500">
        {{ data.mesasge }} | {{ data.count }}
    </p>
  
    <p>
        <ChildComponent/>
    </p>
    <p>
        <ChildComponentX/>
    </p>

</template>
<style scoped></style>