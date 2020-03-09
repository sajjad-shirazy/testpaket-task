<template>
    <div>
        <Navbar />
        <b-container>
            <br />
            <h1>Test diapers and wet wipes</h1>
            <hr />
            <Product />
        </b-container>
    </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Product from './components/product/Product.vue';

export default {
    name: 'App',
    components: {
        Navbar,
        Product,
    },
};
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
