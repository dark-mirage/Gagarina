<script setup lang="ts">
import {defineComponent,type PropType} from 'vue';
import InfoComponent from './InfoComponent.vue';
</script>

<template>
 <div>
    <div class="section-background container"
    :style="{backgroundImage: `url(${backgroundImage})`}">
        <div
         class="section__text"
         v-for="(sectionItem,sectionIndex) in sectionItems"
         :key="sectionIndex">
            <h1 class="section__h1">
              {{sectionItem.header}}
            </h1>
            <p class="section__paragraph">
              {{sectionItem.text}}
            </p>
        </div>
      <InfoComponent :items="items"/>
    </div>
 </div>
</template>

<style lang="scss">
.section-background {
    position: relative;
    min-height: 477px;
    color: white;
    height: 313px;
    background: linear-gradient(
      136.74deg,
      rgb(0, 0, 0) -5.914%,
      rgba(0, 0, 0, 0) 58.153%
    );
    background-size: cover;
    background-position: center;
}

.section__h1 {
  font-size: 56px;
  font-weight: 700;
  line-height: 68px;
}

.section__paragraph {
  font-size: 24px;
  font-weight: 700;
  line-height: 29px;
}
</style>

<script lang="ts">
export interface SectionList {
  header: string,
  text: string,
}

 export default {
    components: {
        InfoComponent
    },
    props: {
        backgroundImage: String,
        sectionItems: Array as PropType <SectionList[]>
    }
 }
</script>