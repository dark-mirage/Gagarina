<script setup lang="ts">
import { defineComponent } from 'vue'
import TradeInComponent from '../components/TradeInComponent.vue';
import InfoComponent from '../components/InfoComponent.vue';
</script>

<template>
  <div class="home__container flex-column">
    <div>
      <TradeInComponent/>
    </div>
    <div>
      <InfoComponent/>
    </div>
  </div>
</template>

<style lang="scss">
  .home__container {
    gap: 40px
  }
</style>

<script lang="ts">
export default {
  name: 'HomeView',
  components : {
    TradeInComponent,
    InfoComponent
  }
}
</script>