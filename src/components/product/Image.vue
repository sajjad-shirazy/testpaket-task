<template>
    <img :src="`img/${src}`" />
</template>
<script>
export default {
    props: ['size'],
    computed: {
        src() {
            switch (this.size) {
                case '2-5 KG':
                    return 'lillydoo-testpaket-10.jpg';
                case '4-8 KG':
                    return 'lillydoo-testpaket-20.jpg';
                case '6-10 KG':
                    return 'lillydoo-testpaket-30.jpg';
                case '9-14 KG':
                    return 'lillydoo-testpaket-40.jpg';
                case '11-16 KG':
                    return 'lillydoo-testpaket-50.jpg';
                default:
                    return '';
            }
        },
    },
};
</script>

<style lang="scss" scoped>
img {
    width: 100%;
    margin-bottom: 24px;
}
</style>
