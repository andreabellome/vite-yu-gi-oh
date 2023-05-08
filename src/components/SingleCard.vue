<script>

export default {
    name: 'SingleCard',
    props: ['datiSingolaCard']
}
</script>

<template>
    <div class="card col-12 col-md-6 col-lg-3 mb-2">
        <img :src="datiSingolaCard.card_images[0].image_url" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{ datiSingolaCard.name }}</h5>
            <span class="card-text">{{ datiSingolaCard.archetype }}</span>
        </div>
    </div>
</template>



<style lang="scss" scoped></style>