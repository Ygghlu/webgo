<template>
    <v-container>


    </v-container>

    <v-card class="card">
        <v-row no-gutters>
            <v-col cols="5" justify="center" align="center">
                <v-img :src="product.image" alt="product Image" class="mx-auto my-7 pa-2 " align="center"
                    max-width="400px"></v-img>
            </v-col>
            <v-col cols="6" offset="0" class="p-7">
                <div></div>
                <v-row class="pa-2 ma-2">
                    <h2 class="font-weight-bold text-grey-darken-4">{{ product.title }}</h2>

                </v-row>
                <v-row class="pa-2 ma-2">
                    <p class="text-xl ">Price - ${{ product.price }}</p>
                </v-row>
                <v-row class="pa-2 ma-2">
                    <h3>Product Description:</h3>
                    <v-divider></v-divider>
                    <p>{{ product.description }}</p>

                </v-row>
                <v-btn @click="addToCart(product)">
                    <i class="material-icons mr-2">add_shopping_cart</i>
                    <span>Add to cart</span>
                </v-btn>
            </v-col>


        </v-row>

    </v-card>
</template>

<script setup >
const { product } = defineProps(['product'])
const shoppingCart = []

function addToCart() {

    this.shoppingCart.push({
        ...product,

    })
    //console.log(product.description)
    //console.log(shoppingCart)
    localStorage.setItem('shoppingCart', JSON.stringify(shoppingCart))
}


</script>

<style></style>