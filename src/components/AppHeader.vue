<script>
export default {

    data() {
        return {
            navElems: [
                {
                    linkName: "CHARACTERS",
                    linkDir: "#",
                },
                {
                    linkName: "COMICS",
                    linkDir: "#",
                },
                {
                    linkName: "MOVIES",
                    linkDir: "#",
                },
                {
                    linkName: "TV",
                    linkDir: "#",
                },
                {
                    linkName: "GAMES",
                    linkDir: "#",
                },
                {
                    linkName: "COLLECTIBLES",
                    linkDir: "#",
                },
                {
                    linkName: "VIDEOS",
                    linkDir: "#",
                },
                {
                    linkName: "FANS",
                    linkDir: "#",
                },
                {
                    linkName: "NEWS",
                    linkDir: "#",
                },
                {
                    linkName: "SHOP",
                    linkDir: "#",
                }
            ],
            logo: "dc-logo",
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}.png`, import.meta.url).href;
        }
    }
}

</script>

<template>
    <header>
        <div>
            <div class="firstCont">
                <img :src="getImagePath(logo)" alt="">
            </div>
            <div class="SecondContainer">
                <ul>
                    <li v-for="Elem in navElems" :key="index">
                        <a :href="Elem.linkDir">
                            {{ Elem.linkName }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>

    </header>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
    width: 100%;
    height: 15vh;
    background-color: #fff;
    

    div {

        margin: 0 auto;
        @include flex(row, space-between, center);
        max-width: 1200px;
        height: 15vh;
        background-color: #fff;

        .firstCont {
            img {
                width: 5vw;
            }
        }

        .SecondContainer {
            ul {
                @include flex(row, center, center);
                list-style-type: none;
                

                li {
                    padding: 0 1.2vw;
                    line-height: 14.3vh;
                    
                    &:hover {

                        border-bottom: 5px solid $color_lightBlue;
                        transition: ease-in .2s;
                        
                        
                    }
                    a {
                        font-size: .9vw;
                        text-decoration: none;
                        color: inherit;
                        


                    }
                }
            }
        }
    }

}</style>