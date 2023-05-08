<script>
import axios from 'axios'
import { store } from '../store'

import SingleCard from './SingleCard.vue'

export default {
    name: 'CardComp',
    components: {
        SingleCard
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="main-div-style">

        <div class="inner-div-style">

            <div class="bg-dark col-white padd-5">
                Found {{ store.arrayCards.length }} cards
            </div>

            <div class="padd-10 row">
                <SingleCard v-for="(elem, index) in store.arrayCards" :key="index" :datiSingolaCard="elem" />
            </div>

        </div>

    </div>
</template>



<style lang="scss" scoped>
.main-div-style {
    background-color: orange;
    padding: 10px;

    display: flex;
    justify-content: center;
}

.inner-div-style {
    background-color: #FFFFFF;
    width: 80%;
    padding: 10px;
}
</style>