<template>

    <v-card align="center" p-3 rounded-md bg-white shadow-md h-full>

        <img :src="product.image" alt="Product thumbnails" class="thumb">
        <p class="font-weight-bold text-grey-darken-4">{{ product.title }}</p>
        <NuxtLink :to="`/product/${product.id}`"> <v-btn> Detail </v-btn> </NuxtLink>



    </v-card>

</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style>
.thumb {
    max-height: 120px;
    max-width: 70%;
    margin: 2;
}


</style>