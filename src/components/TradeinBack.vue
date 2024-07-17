<template>
 <div class="trade-inback container">
    <div class="car-back background">
        <div class="span">
            Ставка от<br>
            4.9
        </div>
    </div>
 </div>
</template>

<style lang="scss">

.trade-inback {
    position: relative;
}

.background {
    background-position: center;
    background-repeat: no-repeat;
}

.span {
    position: absolute;
    top: -40;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 177px;
    height: 177px;
    font-size: 20px;
    font-weight: 600;
    background-color: white;
    border-radius: 50%;
    box-shadow: 0 0 20px -10px;
}

.car-back {
    position: absolute;
    top: 51px;
    left: 80px;
    width: 627px;
    height: 289px;
    background-image: url('../assets/images/car.jpg');
    background-position-y: center;
}

@media (max-width: 1730px) {
    .car-back {
        width: 500px;
        background-position: center;
        background-size: contain;
    }
}

@media(max-width: 1570px) {
    .car-back {
        left: -100px
    }
}

@media(max-width: 1160px) {
    .car-back {
        left: -200px;
    }
}

@media(max-width: 782px) {
    .car-back {
        left: -220px;
    }

}

@media(max-width: 580px) {
    .car-back {
        width: 332px;
        height: 153px;
        left: -130px;
        top: 80px;
    }

    .span {
        width: 140px;
        height: 140px;
        left: -40px;
        top: -40px;
    }
}
</style>

<script lang="ts">
 export default {

 }
</script>

