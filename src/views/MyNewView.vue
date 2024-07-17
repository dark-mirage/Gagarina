<script setup lang="ts">
import { defineComponent } from 'vue';
import RangeComponent from '../components/RangeComponent.vue'
</script>


<template>
 <div class="container">
    <RangeComponent/>
 </div>
</template>

<script lang="ts">
 export default {
    name: 'MyNewView',
    components: {
        RangeComponent
    }
 }
</script>

<style lang="scss">
.grid {
   display: grid;
   padding-top: 20px;
   grid-template-areas: "text-1 text-1 text-1"
   "text-2 text-3 text-4"
   "text-5 text-5 text-5"
}

.text-1  {
    background-color: red;
    grid-area: text-1;
}

.text-2  {
    background-color: rgb(45, 0, 168);
    grid-area: text-2;
}

.text-3  {
    background-color: rgb(251, 255, 0);
    grid-area: text-3;
}

.text-4  {
    background-color: rgb(204, 0, 255);
    grid-area: text-4;
}

.text-5  {
    background-color: rgb(30, 255, 0);
    grid-area: text-5;
}
</style>