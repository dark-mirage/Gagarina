<script>
</script>

<template>
 <div class="info-container container">
    <ul class="info__list flex">
        <li class="info__item flex-column">
            <img class="info__svg" src="../assets/images/info-1.svg" alt="info-svg">
            <span class="info__span">
                TRADE IN&nbsp;как первый взнос
            </span>
        </li>
        <li class="info__item flex-column">
            <img class="info__svg" src="../assets/images/info-2.svg" alt="info-svg">
            <span class="info__span">
                Выгода до&nbsp;250 000₽
            </span>    
        </li>
        <li class="info__item flex-column">
            <img class="info__svg" src="../assets/images/info-3.svg" alt="info-svg">
            <span class="info__span">
                Диагностика бесплатно
            </span>
        </li>
        <li class="info__item flex-column">
            <img class="info__svg" src="../assets/images/info-4.svg" alt="info-svg">
            <span class="info__span">
                Выкупаем дорого
            </span>
        </li>
    </ul>
 </div>
</template>

<script>
 export default {

 }
</script>

<style lang="scss">

.info-container {
    position: absolute;
    padding: 0;
    bottom: -100px;
    left: 550px;
}


.info__list {
    padding: 32px 20px;
    color: black;
    background-color: white;
    box-shadow: 0 4px 30px 0 rgba(0,0,0,0.1)
}

.info__item {
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
</style>