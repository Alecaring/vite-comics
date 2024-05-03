
<!-- !DA UNSERIRE L'IMMAGINE DEL CONTENITORE DINAMICAMENTE (LEFT) && footer bottom -->




<script>
export default {

    data() {
        return {
            firstFooterElems: [
                {
                    linkTitle: "DC COMICS",
                    link: "#"
                },
                {
                    linktxt: "Characters",
                    link: "#"
                },
                {
                    linktxt: "Comics",
                    link: "#"
                },
                {
                    linktxt: "Movies",
                    link: "#"
                },
                {
                    linktxt: "TV",
                    link: "#"
                },
                {
                    linktxt: "Gamnes",
                    link: "#"
                },
                {
                    linktxt: "Videos",
                    link: "#"
                },
                {
                    linktxt: "News",
                    link: "#"
                },
            ],
            SecondFooterElems: [
                {
                    linkTitle: "SHOP",
                    link: "#"
                },
                {
                    linktxt: "Shop DC",
                    link: "#"
                },
                {
                    linktxt: "Shop DC Collection",
                    link: "#"
                },
            ],
            ThirdFooterElems: [
                {
                    linkTitle: "DC",
                    link: "#"
                },
                {
                    linktxt: "Terms Of Use",
                    link: "#"
                },
                {
                    linktxt: "Privacy Policy (New)",
                    link: "#"
                },
                {
                    linktxt: "Ad Choises",
                    link: "#"
                },
                {
                    linktxt: "Advertising",
                    link: "#"
                },
                {
                    linktxt: "Jobs",
                    link: "#"
                },
                {
                    linktxt: "Subscriptions",
                    link: "#"
                },
                {
                    linktxt: "Talent Workshops",
                    link: "#"
                },
                {
                    linktxt: "CPSC Certificates",
                    link: "#"
                },
                {
                    linktxt: "Ratings",
                    link: "#"
                },
                {
                    linktxt: "Shop Help",
                    link: "#"
                },
                {
                    linktxt: "Contact Us",
                    link: "#"
                },
            ],
            fourthFooterElems: [
                {
                    linkTitle: "SITES",
                    link: "#"
                },
                {
                    linktxt: "DC",
                    link: "#"
                },
                {
                    linktxt: "MAD Magazine",
                    link: "#"
                },
                {
                    linktxt: "DC Kids",
                    link: "#"
                },
                {
                    linktxt: "DC Universe",
                    link: "#"
                },
                {
                    linktxt: "DC Power Visa",
                    link: "#"
                },
            ],
        }
    },
    methods: {

    }
}
</script>

<template>
    <section>
        <div class="MainCont">

            <div class="imgContainer">
                <img class="bg_animation" src="../assets/img/footer-bg.jpg" alt="">
            </div>

            <div class="firtInnerCont">
                <ul>
                    <li>
                        <h4>
                            {{ firstFooterElems[0].linkTitle }}
                        </h4>
                    </li>
                    <li v-for="Elem in firstFooterElems" :key="index">
                        <a :href="Elem.link">
                            {{ Elem.linktxt }}
                        </a>
                    </li>
                </ul>
                <ul>
                    <li>
                        <h4>
                            {{ SecondFooterElems[0].linkTitle }}
                        </h4>
                    </li>
                    <li v-for="Elem in SecondFooterElems" :key="index">
                        <a :href="Elem.link">
                            {{ Elem.linktxt }}
                        </a>
                    </li>
                </ul>
                <ul>
                    <li>
                        <h4>
                            {{ ThirdFooterElems[0].linkTitle }}
                        </h4>
                    </li>
                    <li v-for="Elem in ThirdFooterElems" :key="index">
                        <a :href="Elem.link">
                            {{ Elem.linktxt }}
                        </a>
                    </li>
                </ul>
                <ul>
                    <li>
                        <h4>{{ fourthFooterElems[0].linkTitle }}</h4>
                    </li>
                    <li v-for="Elem in fourthFooterElems" :key="index">
                        <a :href="Elem.link">
                            {{ Elem.linktxt }}
                        </a>
                    </li>
                    <!-- <li><a href="#">MAD Magazine</a></li>
                    <li><a href="#">DC Kids</a></li>
                    <li><a href="#">DC Universe</a></li>
                    <li><a href="#">DC Power Visa</a></li> -->

                </ul>

            </div>
            <div class="secondInnerCont">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>

        <div class="footerBottom">
            <div class="innerFooterBottom">
                <span>
                    <a href="#">SIGN-UP NOW!</a>
                </span>
                <ul>
                    <li><a href="#">
                            <h4>FOLLOW US</h4>
                        </a></li>
                    <li><a href="#">
                            <span><img src="../assets/img/footer-facebook.png" alt=""></span>
                        </a></li>
                    <li><a href="#">
                            <span><img src="../assets/img/footer-periscope.png" alt=""></span>
                        </a></li>
                    <li><a href="#">
                            <span><img src="../assets/img/footer-pinterest.png" alt=""></span>
                        </a></li>
                    <li><a href="#">
                            <span><img src="../assets/img/footer-twitter.png" alt=""></span>
                        </a></li>
                    <li><a href="#">
                            <span><img src="../assets/img/footer-youtube.png" alt=""></span>
                        </a></li>
                </ul>
            </div>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

section {
    width: 100%;

    .MainCont {
        @include flex(row, center, center);
        height: 45vh;
        width: 100%;
        max-width: 1000px;
        margin: 0 auto;

        .imgContainer {
            position: absolute;
            z-index: -1;
            width: 100%;
            height: 45vh;
            object-fit: cover;
            overflow: hidden;

            .bg_animation {
                width: 100%;

                -webkit-animation: bg_animation 15s ease-out infinite alternate-reverse both;
                animation: bg_animation 15s ease-out infinite alternate-reverse both;
            }

            @-webkit-keyframes bg_animation {
                0% {
                    -webkit-transform: scale(1) translate(0, 0);
                    transform: scale(1) translate(0, 0);
                    -webkit-transform-origin: 84% 84%;
                    transform-origin: 84% 84%;
                }

                100% {
                    -webkit-transform: scale(1.25) translate(20px, 15px);
                    transform: scale(1.25) translate(20px, 15px);
                    -webkit-transform-origin: right bottom;
                    transform-origin: right bottom;
                }
            }

            @keyframes bg_animation {
                0% {
                    -webkit-transform: scale(1) translate(0, 0);
                    transform: scale(1) translate(0, 0);
                    -webkit-transform-origin: 84% 84%;
                    transform-origin: 84% 84%;
                }

                100% {
                    -webkit-transform: scale(1.25) translate(20px, 15px);
                    transform: scale(1.25) translate(20px, 15px);
                    -webkit-transform-origin: right bottom;
                    transform-origin: right bottom;
                }
            }
        }

        .firtInnerCont {
            @include flex(column, flex-start, flex-start);
            flex-wrap: wrap;
            width: 50%;
            height: 100%;

            ul {
                list-style-type: none;
                padding: 2vw;

                li {
                    h4 {
                        color: white;
                        padding-bottom: 1.5vw;
                        font-size: 1vw;
                    }

                    a {
                        text-decoration: none;
                        color: rgb(181, 163, 163);
                        font-size: .7vw;
                    }
                }
            }
        }

        .secondInnerCont {
            position: relative;
            width: 50%;
            height: 100%;
            overflow: hidden;

            img {
                width: 90%;
                position: absolute;
                top: 0;
                left: 0;
                transform: translate(5%, -15%);
            }
        }
    }

    .footerBottom {
        width: 100%;
        padding: 2vw;
        background-color: $color_dark;

        .innerFooterBottom {
            @include flex(row, space-between, center);
            max-width: 1000px;
            margin: 0 auto;



            span {
                a {
                    background-color: transparent;
                    border: 1.5px solid $color_lightBlue;
                    padding: 1vw 1.5vw;
                    color: white;
                    text-decoration: none;
                    font-size: 1.4vw
                }
            }

            ul {
                @include flex(row, center, center);
                list-style-type: none;
                gap: 20px;

                li {
                    a {
                        text-decoration: none;

                        h4 {
                            padding: 0 2vw;
                            color: $color_lightBlue;
                            font-size: 1.4vw;
                        }

                        span {
                            display: inline-block;
                            width: 4vw;
                            height: 4vw;
                            background-color: transparent;

                            img {
                                object-fit: cover;
                                width: 100%;
                            }
                        }
                    }
                }
            }
        }


    }
}
</style>