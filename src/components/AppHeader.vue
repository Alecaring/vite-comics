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
            ]
        }
        methods: {

        }
    },

}

</script>

<template>
    <header>


        <div class="firstCont">
            <img src="../assets/img/dc-logo.png" alt="">
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

    </header>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
    width: 100%;
    max-width: 1000px;
    margin: 0 auto;
    @include flex(row, space-between, center);
    padding: 2rem 0;

    .firstCont {
        img {
            width: 5vw;
        }
    }

    .SecondContainer {
        ul {
            @include flex(row, center, center);
            list-style-type: none;
            gap: 2vw;

            li {

                a {
                    font-size: .9vw;
                    text-decoration: none;
                    color: inherit;

                }
            }
        }
    }
}
</style>