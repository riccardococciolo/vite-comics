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
            height: 200px;
            object-fit: cover;
            object-position: top;
        }
        
        span {
            display: inline-block;
            padding-top: 1rem;
        }
    }
    
</style>