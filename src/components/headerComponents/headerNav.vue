<template>
    <section class="w-full bg-blue-950 py-2 flex items-center justify-center">
        
        <input class="w-3/5 rounded-sm px-1" @input="productSearch()" type="text" v-model="searchInput">

        <searchIcon class="translate-x-7"/>

        <!-- show box -->
        <div class="w-3/5 z-20 shadow-sm shadow-gray-400 absolute translate-x-3 -translate-y-1 top-20 bg-white flex justify-center items-center" v-if="searchInput">

            <loader v-if="!foundProduct"/>

            <router-link v-if="foundProduct" to="/">
                
                <div class="w-72 my-4 relative bg-black p-1 rounded-lg flex justify-center items-center overflow-hidden
                hover:-translate-y-4 transition-all ease-linear duration-200">

                <div class="movingLine z-0"></div>

                    <article class="w-full bg-white z-10 group border rounded-lg  flex flex-col justify-center items-center gap-2 overflow-hidden">
                        <figure class="w-full h-40">
                            <img class="w-full h-full" src="@/assets/images/testImage.jpg" alt="productImage">
                        </figure>

                        <div class="w-full grid grid-cols-1 gap-2 text-center p-2 ">
                            <span class="font-bold sm:text-lg">{{ foundProduct.name }}</span>

                            <span class="mb-2">{{ foundProduct.price }}</span>

                            <span class="w-4/5 mx-auto group-hover:w-full transition-all ease-linear duration-200 bg-yellow-900 text-gray-100 rounded p-1">خرید</span>
                        </div>
                    </article>
                </div>

            </router-link>
            
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router';
import loader from '../Icons/loader.vue';
import searchIcon from '../Icons/searchIcon.vue';

let searchInput = ref(null)

let products = [
    {name :'محصول1',price:'12000تومان'},
    {name :'محصول5',price:'11000تومان'},
    {name :'محصول4',price:'14000تومان'},
    {name :'محصول3',price:'15000تومان'},
    {name :'محصول2',price:'16000تومان'},
]
let foundProduct = ref(null)
const productSearch =()=>{
    let searchedProduct = products.find(product=>product.name==searchInput.value)

    foundProduct.value = searchedProduct;

}
</script>

