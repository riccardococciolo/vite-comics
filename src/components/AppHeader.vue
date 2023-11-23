<script>
export default {
    data() {
        return {
            navItems: [
                {
                    title: "characters",
                },
                {
                    title: "comics",
                },
                {
                    title: "movies",
                },
                {
                    title: "tv",
                },
                {
                    title: "games",
                },
                {
                    title: "collectibles",
                },
                {
                    title: "videos",
                },
                {
                    title: "fans",
                },
                {
                    title: "news",
                },
                {
                    title: "shop",
                },
            ]
        }
    },
}
</script>

<template>
    <div class="container">
        <img src="../assets/img/dc-logo.png" alt="">
        <ul>
            <li v-for="(item, index) in navItems">
                <a href="">{{ item.title }}</a>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
    @use '../style/partials/mixin' as *;
    @use '../style/partials/variables' as *;

    .container {
        @include flex(row, space-between);

        img {
            padding: 1rem;
            width: 100px;
        }

        ul {
            list-style: none;
            @include flex();
            gap: 1.5rem;
            font-size: 1.2rem;

            li {
                a {
                    text-decoration: none;
                    color: black;
                }
            }
        }
    }


    
</style>