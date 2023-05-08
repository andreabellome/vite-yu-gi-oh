<script>
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
    <div class="debug main-div-style">

        <div class="debug inner-div-style">

            <div class="bg-dark col-white padd-5">
                Found 30 cards
            </div>

            <div class="debug padd-5">

            </div>

        </div>

    </div>

    <div>
        <SingleCard />
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