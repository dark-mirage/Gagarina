<script setup lang="ts">
import { defineComponent } from "vue";
import TradeInComponent from "../components/TradeInComponent.vue";
import InputComponent, {type InputItem, InputCard } from "../components/InputComponent.vue";
</script>

<template>
  <div class="home__container flex-column">
    <div>
      <TradeInComponent />
    </div>
    <div class="info">
      <InfoComponent class="info-component"/>
    </div>
    <div>
      <InputComponent :items="items" :cards="cards"/>
    </div>
  </div>
</template>

<style lang="scss">

.info {
  margin-bottom: 207px;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media(max-width: 1730px) {
  .container {
    padding: 0 300px;
  }

  .info {
    max-width: 1248px;
  }
}

@media (max-width: 1570px) {
  .container {
    padding: 0 100px;
  }
}
 
@media(max-width: 1160px) {
  .container {
    padding: 0 100px;
  }
}

@media(max-width: 782px) {
  .container {
    padding: 0 16px;
  }
}

</style>

<script lang="ts">
export default {
  name: "HomeView",
  components: {
    TradeInComponent,
    InputComponent
  },
  data() {
    return {
      items: [
        {
          input: 'Марка'
        },
        {
          input: 'Модель'
        },
        {
          input: 'Год'
        }
      ] as InputItem[],
      cards: [
        {
          input: 'ФИО'
        },
        {
          input: 'Телефон'
        },
        {
          input: 'Дата рождения'
        }
      ] as InputCard[]
    }
  }
};
</script>
