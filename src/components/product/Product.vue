<template>
    <b-row>
        <b-col md="6" sm="12">
            <ProductImage :size="selectedSize" />
        </b-col>
        <b-col md="6" sm="12">
            <h2>Discover our skin friendliness</h2>
            <p>CHOOSE YOUR SIZE</p>
            <b-row>
                <b-col
                    v-for="(size, i) in sizes"
                    :key="i"
                    class="size"
                    @click="selectedSize = size.value"
                    :class="{ selected: selectedSize == size.value }"
                >
                    <h4>{{ size.title }}</h4>
                    <small>({{ size.value }})</small>
                </b-col>
            </b-row>
            <hr />
            <p>
                Now test our skin-friendly diapers and receive our wet wipes with 99% water in sizes 1 - 3 or the
                sensitive wet wipes in sizes 4 - 5.
            </p>
            <ol>
                <li>We pay for the products, you only pay for the shipping.</li>
                <li>
                    Automatic transition to diaper subscription that can be canceled at any time for € 49.50 per
                    delivery.
                </li>
                <li>Prices include VAT, plus shipping costs if applicable</li>
            </ol>
            <hr />
            <b-button variant="outline-primary" block size="lg">ADD TO CARD</b-button>
        </b-col>
    </b-row>
</template>

<script>
import ProductImage from './Image.vue';

export default {
    name: 'App',
    data: () => ({
        selectedSize: '2-5 KG',
        sizes: [
            { title: '1', value: '2-5 KG' },
            { title: '2nd', value: '4-8 KG' },
            { title: '3rd', value: '6-10 KG' },
            { title: '4th', value: '9-14 KG' },
            { title: '5', value: '11-16 KG' },
        ],
    }),
    components: {
        ProductImage,
    },
};
</script>
<style lang="scss" scoped>
.size {
    cursor: pointer;
    border: 1px solid #7c7c7c;
    text-align: center;
    width: 30%;
    padding: 7px 5px 2px 5px;
    color: #7c7c7c;
    margin: 3px;
    &:hover,
    &.selected {
        background-color: #00afab;
        border-color: #00afab;
        color: #fff;
    }
}
</style>
