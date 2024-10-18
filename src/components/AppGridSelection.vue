<script>
export default {
    data() {
        return {
            selectionsArray: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}.png`, import.meta.url).href;
        }
    },
}
</script>


<template>
    <div class="txtBtnCont">
        <span><a href="#">CURRENT SERIES</a></span>
    </div>
    <div class="container">
        <div class="innerCont">
            <div v-for="selection in selectionsArray" :key="index" class="cell">
                <img :src="selection.thumb" :alt="selection.series">
                <p>{{ selection.series }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.txtBtnCont {
    width: 80%;
    max-width: 1200px;
    margin: 0 auto;

    span {
        display: inline-block;
        height: 4vw;
        line-height: 4vw;
        padding: 0 2vw;
        position: relative;
        bottom: -2vw;
        background-color: $color_lightBlue;
        font-size: 1vw;
        font-weight: bold;

        &:hover {
            
            border-radius: .5rem;
            transition: ease-in-out .3s;
        }

        a {
            text-decoration: none;
            color: white;
            width: 100%;
            height: 100%;

        }
    }
}

.container {
    width: 100%;
    height: auto;
    background-color: black;
    display: flex;
    justify-content: center;


    .innerCont {

        @include flex (row, center, center);
        flex-wrap: wrap;
        gap: 2vw;
        max-width: 1200px;
        width: 80%;
        height: 100%;
        padding: 10vh 0 2vh 0;

        .cell {
            width: calc(100% / 6 - 2vw);
            height: 40vh;
            border: 1px solid black;
            padding: 3vh 0;

            &:hover {
                opacity: .8;
                border-radius: 1rem;
                transition: ease-in 1sec;

            }

            img {
                width: 100%;
                height: 100%;
                border-radius: 1rem;
                object-fit: cover;
            }

            p {
                color: white;
                margin-bottom: 2vw;
            }
        }
    }


}
</style>