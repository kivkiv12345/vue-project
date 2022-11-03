<script setup>
    defineProps({
        name: {
            type: String,
            required: true
        },
        price: {
            type: Number,
            required: true
        },
        discount: {
            type: Number,
            required: true
        }
    })
</script>

<template>
    <div>
        <h2>
            {{ name }}
        </h2>
        <p v-if="!discount">
            {{ price }}, -DKK
        </p>
        <div v-else>
            <p class="discounted">
                {{ price }}, -DKK
            </p>
            <p>
                {{ discount }}, -DKK
            </p>
        </div>
    </div>
    <slot></slot>
</template>

<style scoped>
    .discounted {
        text-decoration: line-through;
    }
</style>