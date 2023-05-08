<script>

import SingleCard from './SingleCard.vue';

export default {
    name: "MainComponent",
    components: {
        SingleCard
    },
    data() {
        return {
            dcComics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    },
    methods: {

    }
}
</script>

<template>
    <div class=" padd-bottom-5" style="background-color: #1C1C1C;">

        <div class="jumbotron">

            <div class="current-series">
                Current Series
            </div>

        </div>

        <div class="main-div">

            <SingleCard v-for="(comic, index) in dcComics" :key="index" :singleComic="comic" />

        </div>

        <div class="flex just-cont-center padd-20">

            <div class="load-more-button">
                Load More
            </div>

        </div>

    </div>
</template>

<style lang="scss">
.main-div {

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;

    width: 80%;

    margin: auto;
    padding: 5px;

    margin-top: 70px;

    color: #FFFFFF;

}

.jumbotron {
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    background-repeat: no-repeat;

    height: 400px;

    position: relative;

}

.current-series {
    color: #FFFFFF;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 25px;

    display: inline-block;
    position: relative;
    bottom: -95%;
    left: 10%;

    background-color: #0282F9;

    padding: 10px;
}

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
        margin-bottom: 10px;
    }

    span {
        text-transform: uppercase;
        color: #FFFFFF;
    }
}

.load-more-button {
    display: flex;
    justify-content: center;

    width: 10%;
    font-size: 18px;
    padding: 10px;

    text-transform: uppercase;
    font-weight: bold;

    background-color: #0282F9;
    color: #FFFFFF;

    &:hover {
        cursor: pointer;
    }

}
</style>
