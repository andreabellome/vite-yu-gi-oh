<script>
export default {
    name: "HeaderComponent",
    data() {
        return {
            currActive: 1,
            navBarLinks: [
                {
                    nome: 'Characters',
                    current: false
                },
                {
                    nome: 'Comics',
                    current: true
                },
                {
                    nome: 'Movies',
                    current: false
                },
                {
                    nome: 'TV',
                    current: false
                },
                {
                    nome: 'Games',
                    current: false
                },
                {
                    nome: 'Collectibles',
                    current: false
                },
                {
                    nome: 'Videos',
                    current: false
                },
                {
                    nome: 'Fans',
                    current: false
                },
                {
                    nome: 'News',
                    current: false
                },
            ]
        }
    },
    methods: {
        activeChat(index) {
            this.currActive = index;
        }
    }
}
</script>

<template>
    <div class=" bg-white flex align-it-center">

        <div class=" header-div">
            <img src="../assets/img/dc-logo.png" alt="dc-logo" class="img-style padd-5">

            <div class="flex align-it-center flex-wrap padd-5" style="padding-bottom: 0;">
                <div class="div-nav-bar col-dark" v-for="(navLink, index) in navBarLinks"
                    v-bind:class="(currActive == index) ? 'div-nav-bar-clicked' : ''" @click="activeChat(index)">
                    {{ navLink.nome }}
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss">
.div-nav-bar {

    display: flex;
    align-items: center;
    height: 100%;
    margin-right: 5px;
    padding: 5px;
    text-transform: uppercase;

    font-size: 15px;
    font-weight: bold;

    &:hover {
        cursor: pointer;
    }

}

.div-nav-bar-clicked {
    border-bottom: 7px solid #0282F9;
    color: #0282F9;
}

.img-style {
    display: inline-block;
    width: 5%;
    height: 5%;

    &:hover {
        cursor: pointer;
    }
}

.header-div {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;

    width: 80%;

    margin: auto;
    padding: 10px;
    padding-bottom: 0;

}
</style>
