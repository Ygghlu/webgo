<template>




                <v-container fluid col="8">
                    <Head>
                        <Title>Shop Name| {{ product.title }}</Title>
                        <Meta name="description" :content="product.description"/>
                    </Head>

                    <productInfo :product="product" />
                    <ShoppingCart v-model="shoppingCart"/>
                </v-container>


</template>

<script setup>
    definePageMeta({layout:'product'})
    const { id } = useRoute().params
    const uri = 'https://fakestoreapi.com/products/'+ id
    const {data: product} = await useFetch(uri , {key: id})

</script>

<style></style>