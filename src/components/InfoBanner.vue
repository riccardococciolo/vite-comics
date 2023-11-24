<script>
export default {
    data() {
        return {
            icons: [
                {
                    img: "buy-comics-digital-comics.png",
                    text: "digital comics",
                },
                {
                    img: "buy-comics-merchandise.png",
                    text: "dc merchandise",
                },
                {
                    img: "buy-comics-subscriptions.png",
                    text: "sebscription",
                },
                {
                    img: "buy-comics-shop-locator.png",
                    text: "comic shop locator",
                },
                {
                    img: "buy-dc-power-visa.svg",
                    text: "dc power visa",
                },
            ]
        }
    },
    methods: {
        getImageUrl(imgName) {
            return new URL(`../assets/img/${imgName}`, import.meta.url).href;
        }
    },
}
</script>

<template>
    <div class="wrapper">
        <div class="container"> 
            <div v-for="(icon, index) in icons" class="icon-container">
                <img :src="getImageUrl(icon.img)" alt="">
                <span>{{ icon.text }}</span>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.wrapper {
   background-color: $primary;
   position: relative;
   padding: 3rem;
   .container {
        @include flex(row, center, center);
        gap: 2rem;
        color: white;

        .icon-container {
            @include flex(row, center, center);
            gap: 1rem;
            position: relative;
            z-index: 3;
        }

        img {
            height: 50px;
        }
   }
   
}
</style>