<script>

import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import ProductList from './components/ProductList.vue';

export default {
    components: {
    AppHeader,
    AppFooter,
    ProductList,
    ProductList
},
};

</script>

<template>
    <AppHeader />
    <ProductList />
</template>

<style lang="scss">
    @use "./style/general.scss";
</style>
