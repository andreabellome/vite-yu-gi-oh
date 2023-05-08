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
    <div>
        <SingleCard />
    </div>
</template>



<style lang="scss" scoped></style>