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
    <div>
        <img src="" alt="">
        <ul>
            <li v-for="(item, index) in navItems">
                <a href="">{{ item.title }}</a>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
    
</style>