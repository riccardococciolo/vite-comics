<script>
export default {
    props: {
        title: String,
        image: String,
    },
};
</script>

<template>
    <div class="card">
        <img :src="image" alt="">
        <span>{{ title }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

    .card {
        height: 100%;
        img {
            width: 100%;
        }
        
        span {
            text-align: center;
            font-size: 1.3rem;
        }
    }
    
</style>