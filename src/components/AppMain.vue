<script>
export default {

    data() {
        return {
            elemBlueBand: [
                {
                    img: "digital-comics",
                    title: "DIGITAL COMICS",
                },
                {
                    img: "merchandise",
                    title: "DC MERCHANDISE",
                },
                {
                    img: "subscriptions",
                    title: "SUBSCRIPTION",
                },
                {
                    img: "shop-locator",
                    title: "COMIC SHOP LOCATOR",
                },
                {
                    img: "subscriptions",
                    title: "DC POWER VISA",
                }
            ]
        }
    },
}
</script>

<template>
    <main>
        <section class="firstSection">
            <span class="content">
                <h1> -- content goes here -- </h1>
            </span>

        </section>
        <section class="secondSection">
            <div class="bottomSec">
                <ul>
                    <li v-for="elem in elemBlueBand" :key="index"><a href="#">
                            <span>
                                <img src="`../assets/img/buy-comics-digital-comics.png`" alt="">
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
            padding: 4vw;
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

                        span {
                            img {
                                width: 2vw;
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