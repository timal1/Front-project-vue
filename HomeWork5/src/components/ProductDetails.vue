<template>
    <form>
        <h1>Product: {{ product.name }}</h1>
        <p>Price: {{ formattedPrice }}</p>
        <p v-if="product.available">Available</p>
        <p v-else>Out of stock</p>
    </form>
</template>

<script>
export default {
    data() {
        return {
            product:
            {
                name: "Samsung Galaxy",
                price: 800,
                available: true,
            },
        };
    },

    computed: {
        formattedPrice: function () {
            return `$${this.product.price}`;
        }
    }
}


</script>

<style lang="scss" scoped></style>