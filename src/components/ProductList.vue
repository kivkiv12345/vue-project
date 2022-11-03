<template lang="">
    <div>
        <ProductItem v-for="p in productList" :name="p.name" :price="p.price" :discount="p.discount">
            <!-- <template #name>{{p.name}}</template>
            <template #price>{{p.price}}</template> -->
        </ProductItem>
    </div>
</template>
<script>

import ProductItem from './ProductItem.vue'
export default {
    components: {
        ProductItem
    },
    data() {
        return {
            "productList": [
                {
                    name : "Othello lagkage",
                    price: 100,
                    discount: 0
                },
                {
                    name : "Sandkage",
                    price: 50,
                    discount: 0
                },
                {
                    name : "kajkage",
                    price: 250,
                    discount: 195
                }
            ]
        }
    }
}
</script>
<style lang="">
    
</style>