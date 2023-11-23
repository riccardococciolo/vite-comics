<script>
export default {
    data() {
        return {
            footerItems: [
                {
                    title: "dc comics",
                    links: ["characters", "comics", "movies", "tv", "games", "videos", "news"],
                },
                {
                    title: "shop",
                    links: ["shop dc", "shop dc collectibles"],
                },
                {
                    title: "dc",
                    links: ["term of use", "privacy policy(new)", "ad choises", "advertising", "jobs", "subscriptions", "talent workshops", "cpsc certificates", "ratings", "shop help", "contact us"],
                },
                {
                    title: "sites",
                    links: ["dc", "mad magazine", "dc kids", "dc universe", "dc power visa"],
                }
            ]
        }
    },
}
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <div v-for="(item, index) in footerItems">
                <h2>{{ item.title }}</h2>
                <ul>
                    <li v-for="(link, j) in item.links"><a href="">{{ link }}</a></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.wrapper {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    width: 100%;
    position: relative;
    .container {
        padding: 2rem;
        @include flex(row, left, start);
        gap: 1rem;
        color: white;
        ul {
            list-style: none;
            padding: 1rem 0;
            
            li {
                padding: 0.2rem 0;
            }

            a {
                text-decoration: none;
                color: rgb(112, 112, 112);
            }
        }
    }
    &::after {
        content: url(../assets/img/dc-logo-bg.png);
        position: absolute;
        top: -100px;
        right: 100px;
        z-index: 0;
    }
}
</style>