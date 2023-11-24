<script>
export default {
    data() {
        return {
            footerSocial: [
                'footer-facebook.png',
                'footer-twitter.png',
                'footer-youtube.png',
                'footer-periscope.png',
                'footer-pinterest.png',
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
            <div>
                <span class="button"><a href="">sing-up now!</a></span>
            </div>
            <div class="social-container">
                <span>follow us</span>
                <div v-for="(image, index) in footerSocial">
                    <img :src="getImageUrl(image)" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.wrapper {
    background-color: $footer;
    position: relative;
    padding: 2rem;

    .container {
        @include flex(row, space-between, center);

        span {
            color: $primary;
        }

        .button {
            color: white;
            padding: .5rem;
            border: 3px solid $primary;
            a {
                text-decoration: none;
                color: inherit;
            }
        }

        .social-container {
            @include flex(row, center, center);
            gap: 1rem;
        }
    }
}
</style>