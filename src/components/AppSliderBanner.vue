<script>
export default {
    data() {
        return {
            activeIndex: 0,
            slides: [
                {
                    imgs: "jumbotron",
                    title: "title",
                    subtitle: "subtitle",
                },
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}.jpg`, import.meta.url).href;
        },        
    },
}
</script>

<template>
    <section class="banenrContainer">

        <div v-for="slide in slides" :key="index">

            <img :src="getImagePath(slides[activeIndex].imgs)" alt="">
            

        </div>

    </section>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

section {
    div {
        width: 100%;
        height: 40vh;
        object-fit: cover;
        overflow: hidden;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: -1
            ;
        }
    }
}
</style>