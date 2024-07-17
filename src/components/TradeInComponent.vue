<script setup lang="ts">
import { defineComponent } from "vue";
import InfoComponent, { type ListItem } from "../components/InfoComponent.vue";
import SectionBackground from "../components/SectionBackgroundComponent.vue"
</script>

<template>
  <SectionBackground class="section-background" backgroundImage="src/assets/images/tradein.jpg">
  </SectionBackground>
  <InfoComponent :items="items"/>
</template>

<style lang="scss">
</style>

<script lang="ts">

export default {
  name: "TradeInComponent",
  components: {
    InfoComponent,
    SectionBackground
  },
  props: {
        backgroundImage: String,
  },
  data() {
   return {
      items: [
         {
            text: "TRADE IN как первый взнос",
            img: "src/assets/images/info-1.svg"
         },
         {
          text: "Выгода до&nbsp;250 000₽",
          img: "src/assets/images/info-2.svg"
         },
         {
          text: "иагностика бесплатно",
          img: "src/assets/images/info-3.svg"
         },
         {
          text: "Выкупаем дорого",
          img: "src/assets/images/info-4.svg"
         },
      ] as ListItem[],
   }
}
};
</script>
