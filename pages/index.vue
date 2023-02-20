<template>
    <v-container>

        <v-row justify="center" align="center">
            <v-col v-for="p in products" :key="p" cols="6">

                    <ProductCard :product="p" />
                    <!-- <NuxtLink :to="`/product/${p.id}`"> {{ p.title }}</NuxtLink> -->
                    <ShoppingCart v-model="shoppingCart"/>
            </v-col>
        </v-row>

    </v-container>
</template>

<script setup>
const { data: products } = await useFetch('https://fakestoreapi.com/products')
useHead({ 
        title: "Shop name | Homepage",
        meta: [ 
            { name: "description", content: "Shop Description"}
         ]
     })

</script>

<style scoped></style>
