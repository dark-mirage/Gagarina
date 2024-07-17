<script setup lang="ts">
import { defineComponent, type PropType } from 'vue';
</script>

<template>
  <div class="info-container container">
    <ul class="info__list flex">
      <li v-for="(item, index) in items" :key="index"  class="info__item flex-column">
        <img :src="item.img" class="info__svg" />
        <span class="info__span"> {{ item.text }} </span>
      </li>
    </ul>
  </div>
</template>

<style lang="scss">
.info-container {
  height: 50%;
  position: absolute;
  top: 430px;
  left: 0;
  right: 0;
  bottom: -600px;
  margin: 0;
}

.info__list {
  padding: 32px 20px;
  color: black;
  background-color: white;
  box-shadow: 0 4px 30px 0 rgba(0, 0, 0, 0.1);
}

.info__item {
  gap: 10px;
  max-width: 312px;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  padding: 5px 0;
}

.info__item:not(:nth-child(4)) {
  border-right: 1px solid black;
}

.info__svg {
  max-width: 112px;
  max-height: 86px;
}

.info__span {
  font-size: 16px;
  font-weight: 700;
  line-height: 20px;
}

@media (max-width: 1570px) {
  .info__list {
    justify-content: space-between;
  }
}

@media (max-width: 1160px) {

  .info-container {
    overflow: scroll;
  }

  .info__list {
    width: 964px;
    overflow: scroll;
  }
}
</style>

<script lang="ts">
export interface ListItem {
  text: string;
  img: string;
}

export default defineComponent ({
  name: 'InfoComponent',
  props: {
    items: Array as PropType<ListItem[]>,
  },
})

</script>