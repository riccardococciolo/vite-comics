<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <h2>Content goes here</h2>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.wrapper {
    background-color: black;
    z-index: 3;
    position: relative;
}
.container {
    padding: 4rem;
    h2 {
        color: white;
        font-size: 2rem;
    }
}
</style>