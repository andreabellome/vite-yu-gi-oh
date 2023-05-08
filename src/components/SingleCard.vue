<script>

export default {
    name: 'SingleCard',
    props: {
        singleComic: Object
    }
}

</script>

<template>
    <div class="single-card-comic">
        <img :src="singleComic.thumb" :alt="singleComic.series">
        <span>
            {{ singleComic.series }}
        </span>
    </div>
</template>

<style lang="scss">
.single-card-comic {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 10px;

    text-align: center;

    width: calc(100% / 6 - 1%);

    img {
        display: block;
        width: 100%;
        height: 100%;
    }

    span {
        text-transform: uppercase;
        color: #FFFFFF;

        &:hover {
            cursor: pointer;
            color: #0282F9;
        }
    }

    &:hover {
        cursor: pointer;
    }
}
</style>