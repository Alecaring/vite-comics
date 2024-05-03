<script>
export default {

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
                        <h4>DC COMICS</h4>
                    </li>

                    <li><a href="#">Characters</a></li>
                    <li><a href="#">Comics</a></li>
                    <li><a href="#">Movies</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">Gamnes</a></li>
                    <li><a href="#">Videos</a></li>
                    <li><a href="#">News</a></li>
                </ul>
                <ul>
                    <li>
                        <h4>SHOP</h4>
                    </li>

                    <li><a href="#">Shop DC</a></li>
                    <li><a href="#">Shop DC Collection</a></li>
                </ul>
                <ul>
                    <li>
                        <h4>DC</h4>
                    </li>

                    <li><a href="#">Terms Of Use</a></li>
                    <li><a href="#">Privacy Policy (New)</a></li>
                    <li><a href="#">Ad Choises</a></li>
                    <li><a href="#">Advertising</a></li>
                    <li><a href="#">Jobs</a></li>
                    <li><a href="#">Subscriptions</a></li>
                    <li><a href="#">Talent Workshops</a></li>
                    <li><a href="#">CPSC Certificates</a></li>
                    <li><a href="#">Ratings</a></li>
                    <li><a href="#">Shop Help</a></li>
                    <li><a href="#">Contact Us</a></li>
                </ul>
                <ul>
                    <li>
                        <h4>SITES</h4>
                    </li>
                    <li><a href="#">DC</a></li>
                    <li><a href="#">MAD Magazine</a></li>
                    <li><a href="#">DC Kids</a></li>
                    <li><a href="#">DC Universe</a></li>
                    <li><a href="#">DC Power Visa</a></li>

                </ul>

            </div>
            <div class="secondInnerCont">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>

        <div class="footerBottom">
            <div class="innerFooterBottom">
                <span>
                    <button>SIGN-UP NOW!</button>
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
                padding: 1.5rem;

                li {
                    h4 {
                        color: white;
                        padding-bottom: 1rem;
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
        padding: 2rem;
        background-color: $color_dark;

        .innerFooterBottom {
            @include flex(row, space-between, center);
            max-width: 1000px;
            margin: 0 auto;



            span {
                button {
                    background-color: transparent;
                    border: 1.5px solid $color_lightBlue;
                    padding: 1vw 1.5vw;
                    color: white
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
                            font-size: 1.5vw;
                        }

                        span {
                            display: inline-block;
                            width: 40px;
                            height: 40px;
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