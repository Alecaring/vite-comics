<script>
export default {

}
</script>

<template>
    <header>
        

            <div class="firstCont">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <div class="SecondContainer">
                <ul>
                    <li><a href="#">CHARACTERS</a></li>
                    <li><a href="#">COMICS</a></li>
                    <li><a href="#">MOVIES</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">GAMES</a></li>
                    <li><a href="#">COLLECTIBLES</a></li>
                    <li><a href="#">VIDEOS</a></li>
                    <li><a href="#">FANS</a></li>
                    <li><a href="#">NEWS</a></li>
                    <li><a href="#">SHOP</a></li>
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
            @include flex(row, flex-end, center);
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