<script>

import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import ProductList from './components/ProductList.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';
import InfoBanner from './components/InfoBanner.vue';

export default {
    components: {
    AppHeader,
    AppFooter,
    ProductList,
    AppFooterBottom,
    InfoBanner
    },
};

</script>

<template>
    <AppHeader />
    <ProductList />
    <InfoBanner />
    <AppFooter />
    <AppFooterBottom />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
