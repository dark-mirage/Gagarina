<script setup lang="ts">
import { defineComponent } from 'vue';
import Slider from '@vueform/slider';
import "@vueform/slider/themes/default.css";
</script>

<template>
 <div class="range-container container">
    <div class="range__div">
        <div class="range__span-div">
            <span class="range__span">
                Срок кредита
            </span>
            <span class="range__span range__span-2">
                24 месяца
            </span>
        </div>
        <Slider class="range__slider"/>
    </div>
    <div class="range__div">
        <div class="range__span-div">
            <span class="range__span">
                Первоначальный взнос
            </span>
            <span class="range__span range__span-2">
                67 456Р
            </span>
        </div>
        <Slider class="range__slider"/>
    </div>
 </div>
</template>

<style lang="scss">
.range-container {
    display: flex;
    flex-direction: column;
    gap: 40px;
    max-width: 500px;
    width: 500px;
    padding-top: 20px
}

.range__div {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
    gap: 30px
}

.range__span-div {
    display: flex;
    justify-content: space-between
}

.range__span {
    font-size: 16px;
    line-height: 24px;
}

.range__span-2 {
    font-weight: 700;
}
</style>

<script lang="ts">
 export default {
    name: 'FooterComponent',
    components: {
        Slider
    },
    data() {
      return {
        value: 30,
        color: " "
      }
    }
 }
</script>