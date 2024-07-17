<script setup lang="ts">
import defineComponent from 'vue'
import SectionBackgroundComponent,{type SectionList} from "../components/SectionBackgroundComponent.vue";
import InfoComponent from "../components/InfoComponent.vue"
</script>

<template>
 <div class="ransom-container">
   <SectionBackgroundComponent header="Выкуп" text="Выкупаем"/>
   <InfoComponent/>
 </div>
</template>

<style lang="scss">

</style>

<script lang="ts">
 export default {
   name: 'RansomView',
   components: {
      SectionBackgroundComponent,
      InfoComponent
   },
 }
</script>