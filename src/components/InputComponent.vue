<script setup lang="ts">
import { defineComponent, type PropType } from 'vue';
import TradeinBack from '../components/TradeinBack.vue';
</script>

<template>
 <div class="input-container container flex-column">
  <div class="flex input-wrapper">
    <ul class="input__list input__list-1 flex-column">
      <div class="input__wrapper">
        <li class="input__list-item mr-b-40">
          <select class="select input" name="" id="">
            <option value="choose">Выбрать автомобиль</option>
          </select>
        </li>
        <li class="input__list-item mr-b-40">
          <span class="input__list-span input__list-span-1 block">
            ВЗЯТЬ В КРЕДИТ
          </span>
        </li>
        <li class="input__list-item mr-b-8">
          <span class="input__list-span">
            Сдать в TRADE-IN
          </span>
        </li>
      </div>
      <li class="input__list-item grid__item"
      v-for="(item, index) in items"
      :key="index">
        <input class="input" :placeholder="item.input" type="text">
      </li>
    </ul>
    <TradeinBack/>
  </div>
    <ul class="input__list input__list-2 flex">
      <li class="input__list-item input__list-item-2"
      v-for="(card, cicle) in cards"
      :key="cicle">
        <input class="input input-2" :placeholder="card.input" type="text">
      </li>
      <li class="input__list-item-btn flex-column">
        <button class="input__btn">ОТПРАВИТЬ ЗАЯВКУ</button>
        <span class="input__btn-span">Потверждаю наличие гражданства РФ</span>
        <span class="input__btn-span">Согласен на обработку данных</span>
      </li>
    </ul>
 </div>
</template>

<style lang="scss">

.input-container {
  margin-bottom: 40px;
  gap: 40px;
}

.input__list {
  gap: 8px
}

.input__list-2 {
  gap: 20px;
  flex-wrap: wrap;
}

.input__list-span {
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;
  color: rgb(12, 109,69)
}

.input__list-span-1 {
  width: 497px;
  padding-bottom: 8px;
  border-bottom: 1px solid rgb(12,109,69)
}

.select {
  border: none;
}

.input__list-item-2 {
  max-width: 281px;
  width: 100%;
}

.input {
  max-width: 497px;
  width: 100%;
  padding: 16px 12px;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  color: rgb(191, 191, 191);
  background-color: rgb(248, 248,248);
  border-radius: 10px
}

.input-2 {
  width: 100%;
  padding: 16px 12px;
}

.input__btn {
  display: flex;
  justify-content: center;
  width: 281px;
  padding: 16px 12px;
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;
  color: white;
  background-color: rgb(12, 108, 68)
}

.input__btn-span {
  font-size: 12px;
  font-weight: 400;
  line-height: 16px;
}

.input__list-item-btn {
  gap: 8px;
}

@media(max-width: 1160px) {
  .input-container {
    gap: 330px;
  }

  .input-wrapper {
    flex-direction: column;
    left: 450px;
  }

  .input__list {
    justify-content: center;
  }

  .input__list-item {
    display: flex;
    justify-content: center;
  }

}

@media(max-width: 613px) {
  .input__list-item {
    max-width: 100%;
  }

  .input__list-item-btn,
  .input__btn {
    max-width: 497px;
    width: 100%;
  }
}

@media(max-width: 580px) {
  .input-container {
    gap: 250px
  }
}

</style>

<script lang="ts">

export interface InputItem{
  input: string;
}

export interface InputCard{
  input: string;
}

export default {
  name: 'InputComponent',
  component: {
    TradeinBack
  },
  props: {
    items: Array as PropType<InputItem[]>,
    cards: Array as PropType<InputCard[]>
  }
}
</script>