<script>
import AppSliderBanner from './AppSliderBanner.vue';
import AppGridSelection from './AppGridSelection.vue'

export default {
    data() {
        return {
            elemBlueBand: [
                {
                    img: "buy-comics-digital-comics",
                    title: "DIGITAL COMICS",
                    link: "#",
                },
                {
                    img: "buy-comics-merchandise",
                    title: "DC MERCHANDISE",
                    link: "#",
                },
                {
                    img: "buy-comics-subscriptions",
                    title: "SUBSCRIPTION",
                    link: "#",
                },
                {
                    img: "buy-comics-shop-locator",
                    title: "COMIC SHOP LOCATOR",
                    link: "#",
                },
                {
                    img: "buy-comics-merchandise",
                    title: "DC POWER VISA",
                    link: "#",
                }
            ]
        };
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}.png`, import.meta.url).href;
        }
    },
    components: {
         AppSliderBanner, 
         AppGridSelection 
        }
}
</script>

<template>
    <main>
        <section>
            <AppSliderBanner />
            <AppGridSelection />
        </section>
        <section class="firstSection">
            <span class="content">
                <h1> -- content goes here -- </h1>
            </span>

        </section>
        <section class="secondSection">
            <div class="bottomSec">
                <ul>
                    <li v-for="elem in elemBlueBand" :key="index">
                        <a :href="elem.link">
                            <span>
                                <img :src="getImagePath(elem.img)" :alt="elem.title">
                            </span>
                            <p>
                                {{ elem.title }}
                            </p>
                        </a>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
@use "../style/general.scss" as *;

main {

    .firstSection {
        background-color: black;
        width: 100%;

        .content {
            max-width: 1000px;
            @include flex(row, flex-start, center);
            margin: 0 auto;


            h1 {
                color: white;
                padding: 3rem 0;
            }
        }
    }

    .secondSection {
        background-color: $color_lightBlue;
        width: 100%;


        .bottomSec {
            margin: 0 auto;
            padding: 3vw;
            max-width: 1000px;

            ul {
                @include flex (row, space-between, center);
                list-style-type: none;

                li {
                    a {
                        @include flex (row, space-between, center);
                        gap: 1vw;
                        text-decoration: none;
                        color: white;

                        &:hover {
                            color: rgb(255, 192, 84);
                            transition: ease-in-out .3s;
                        }

                        span {
                            img {
                                height: 2vw;
                            }
                        }

                        p {
                            font-size: .8vw;
                        }
                    }
                }
            }
        }
    }
}
</style>