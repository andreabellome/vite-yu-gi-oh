<script>
export default {
    name: "FooterComponent",
    data() {
        return {
            footBarLinks: [
                {
                    nome: 'Digital Comics',
                    current: false,
                    imgUrl: '../src/assets/img/buy-comics-digital-comics.png'
                },
                {
                    nome: 'DC Merchandise',
                    current: true,
                    imgUrl: '../src/assets/img/buy-comics-merchandise.png'
                },
                {
                    nome: 'Subscription',
                    current: false,
                    imgUrl: '../src/assets/img/buy-comics-subscriptions.png'
                },
                {
                    nome: 'Comic Shop Locator',
                    current: false,
                    imgUrl: '../src/assets/img/buy-comics-shop-locator.png'
                },
                {
                    nome: 'DC Power Visa',
                    current: false,
                    imgUrl: '../src/assets/img/buy-dc-power-visa.svg'
                }
            ]
        }
    },
    methods: {

    }
}
</script>

<template>
    <div class="bg-blue-dc flex align-it-center padd-top-20 padd-bottom-20">

        <div class="footer-div">

            <div class=" footer-card" v-for="(footLinks, indexfoot) in footBarLinks" style="width: calc(100%/5 - 1%);">

                <img v-bind:src="footLinks.imgUrl" v-bind:alt="footLinks.nome"
                    style="display: inline-block; width: 18%; margin-right: 5px;">

                <span class="col-white">
                    {{ footLinks.nome }}
                </span>

            </div>

        </div>
    </div>

    <div class=" bg-foot-main">
        <div class=" footer-div bg-img-dc padd-top-40 padd-bottom-40">

            <div class=" flex flex-dir-row">

                <div class=" flex flex-dir-col mr-30">
                    <ul class=" padd-5 mb-20">
                        <li class="mb-20 text-uppercase text-bold col-white font-size-18">
                            DC Comics
                        </li>
                        <li>
                            <a href="#">
                                Characters
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Comics
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Movies
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                TV
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Games
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Videos
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                News
                            </a>
                        </li>
                    </ul>

                    <ul class=" padd-5 ">
                        <li class="mb-20 text-uppercase text-bold col-white font-size-18">
                            Shop
                        </li>
                        <li>
                            <a href="#">
                                Shop DC
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Shop DC Collectibles
                            </a>
                        </li>
                    </ul>
                </div>

                <ul class=" padd-5 mr-30">
                    <li class="mb-20 text-uppercase text-bold col-white font-size-18">
                        Terms of Use
                    </li>
                    <li>
                        <a href="#">
                            Privacy Policy (New)
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Ad Choices
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Advertising
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Jobs
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Subscriptions
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Talent Workshops
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            CPSC Certificates
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Ratings
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Shop Help
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            Contact us
                        </a>
                    </li>
                </ul>

                <ul class=" padd-5">
                    <li class="mb-20 text-uppercase text-bold col-white font-size-18">
                        Sites
                    </li>
                    <li>
                        <a href="#">
                            DC
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            MAD Magazine
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            DC Kids
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            DC Universe
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            DC Power Visa
                        </a>
                    </li>
                </ul>

            </div>

        </div>
    </div>

    <div class="bg-grey-dc flex align-it-center padd-top-10 padd-bottom-10">
        <div class="footer-div">

            <div class="sign-up ">
                Sign-Up Now!
            </div>

            <div class="flex align-it-center padd-5">

                <div class="follow-us">
                    Follow Us
                </div>

                <div class="footer-logos">
                    <img src="../assets/img/footer-facebook.png" alt="footer-facebook" class="mr-10">

                    <img src="../assets/img/footer-twitter.png" alt="footer-twitter" class="mr-10">

                    <img src="../assets/img/footer-youtube.png" alt="footer-youtube" class="mr-10">

                    <img src="../assets/img/footer-pinterest.png" alt="footer-pinterest" class="mr-10">

                    <img src="../assets/img/footer-periscope.png" alt="footer-periscope">
                </div>
            </div>

        </div>
    </div>
</template>

<style lang="scss">
ul {
    list-style-type: none;
}

ul li {
    color: #FFFFFF;
}

ul li a {
    font-size: 15px;
    color: #675E5E;

    &:hover {
        color: #0282F9;
    }
}

.bg-blue-dc {
    background-color: #0282F9;
}

.bg-grey-dc {
    background-color: #303030;
}

.bg-foot-main {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

.footer-card {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    text-transform: uppercase;
    font-size: 15px;

    padding: 5px;

    &:hover {
        cursor: pointer;
        border: 1px solid #FFFFFF;
        border-radius: 20px;
    }

}

.sign-up {
    display: flex;
    align-items: center;
    color: #FFFFFF;
    text-transform: uppercase;
    font-size: 18px;
    padding: 10px;
    border: 3px solid #0282F9;

    &:hover {
        cursor: pointer;
    }
}

.footer-div {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;

    width: 80%;

    margin: auto;
    padding: 5px;

}

.follow-us {

    text-transform: uppercase;
    font-size: 20px;
    font-weight: bold;
    margin-right: 10px;
    color: #0282F9;

    &:hover {
        cursor: pointer;
    }
}

.bg-img-dc {
    background-image: url('../assets/img/dc-logo-bg.png');
    background-repeat: no-repeat;
    background-size: 40%;
    background-position: center right;
}

.footer-logos {
    img {
        &:hover {
            cursor: pointer;
        }
    }
}
</style>
