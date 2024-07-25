<template>
    <router-link to="/">
        <div class="relative bg-black p-1 rounded-lg flex justify-center items-center overflow-hidden
        hover:-translate-y-4 transition-all ease-linear duration-200">

            <div class="movingLine z-0"></div>

            <article class="w-full bg-white z-10 group border rounded-lg  flex flex-col justify-center items-center gap-2 overflow-hidden">
                <figure class="w-full h-40">
                    <img class="w-full h-full" src="@/assets/images/testImage.jpg" alt="productImage">
                </figure>

                <div class="w-full grid grid-cols-1 gap-2 text-center p-2 ">
                    <span class="font-bold sm:text-lg">{{ product.name }}</span>

                    <span class="mb-2">{{ product.price }}</span>

                    <span class="w-4/5 mx-auto group-hover:w-full transition-all ease-linear duration-200 bg-yellow-900 text-gray-100 rounded p-1">خرید</span>
                </div>
            </article>
        </div>
        

    </router-link>
</template>

<script setup>
import {RouterLink} from 'vue-router';
import {ref} from 'vue';

const props = defineProps(['product']);

</script>

<style>
.movingLine {
    width: 200%;
    height: 4px;
    background-color: white;
    box-shadow: 1px 1px 1px 10px white ;
    transform: rotate(-38deg);
    position: absolute;
    animation: lineAnimation 3s linear infinite;
}
@keyframes lineAnimation {
    0% {
        left: -95%;
        top: -4%;
    }
    30% {
        left: 95%;
        top: 130%;
    }
    100% {
        left: 95%;
        top: 130%;
    }
}
</style>