<script setup lang="ts">
import { defineComponent } from 'vue'
import InfoComponent from '../components/InfoComponent.vue'
</script>

<template>
 <div class="tradeIn-container container">
    <h1 class="tradeIn__h1">
        Trade&nbsp;in
    </h1>
    <p class="tradeIn__paragraph">
        Выгода до&nbsp;250&nbsp;000
        как первоначальный взнос
    </p>
    <InfoComponent/>
 </div>
</template>

<style lang="scss">
.tradeIn-container {
    position: relative;
    padding-top: 22px;
    padding-bottom: 313px;
    color: white;
    background: linear-gradient(136.74deg, rgb(0, 0, 0) -5.914%,rgba(0, 0, 0, 0) 58.153%),url('../assets/images/tradein.jpg');
    background-size: cover;
    background-position: center;
}

.tradeIn__h1 {
    font-size: 56px;
    font-weight: 700;
    line-height: 68px;
}

.tradeIn__paragraph {
    font-size: 24px;
    font-weight: 700;
    line-height: 29px;
}
</style>

<script lang="ts">
 export default {
    name: 'TradeInComponent',
    components: {
        InfoComponent
    }
 }
</script>