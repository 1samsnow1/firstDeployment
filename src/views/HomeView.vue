<template>

  <section class="md:w-4/5 w-11/12 max-w-5xl mx-auto flex flex-col justify-center items-center my-10">

    <h2 class="text-lg md:text-xl font-bold flex items-end gap-1 mb-2">
      محصولات
      <img class="w-8 h-8" src="@/assets/images/productIcon.png" alt="productIcon">
    </h2>
    <!-- orange line -->
    <div class="w-full theShadow mb-8"></div>

     <!-- product box -->
    <section class="w-full grid grid-cols-2 sm:grid-cols-4 md:gap-8 gap-4 rounded-lg sm:p-4 sm:shadow-lg shadow-gray-800">
      <productCard v-for="product in productList" :key="product" :product="product"/>
    </section>

  </section>

</template>

<script setup>
import productCard from '@/components/homeComponents/productCard.vue';
let productList = [
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول1',price:'12000 تومان'},
  {name:'محصول2',price:'12000 تومان'},
  {name:'محصول2',price:'12000 تومان'},
  {name:'محصول2',price:'12000 تومان'},
  {name:'محصول2',price:'12000 تومان'},
  {name:'محصول2',price:'12000 تومان'},
  {name:'محصول2',price:'12000 تومان'},
  {name:'محصول3',price:'12000 تومان'},
  {name:'محصول4',price:'12000 تومان'},
  {name:'محصول5',price:'12000 تومان'},
]
</script>

<style scoped>
.theShadow {
  box-shadow: 0px 1px 0 1px rgb(255, 174, 23);
}
</style>