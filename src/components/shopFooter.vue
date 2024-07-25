<template>
    <section class="w-full bg-blue-950 flex justify-around items-center gap-2 py-5">

        <div v-for="item in footerList" class="text-gray-300 text-sm sm:text-lg">
            <span class="font-bold">{{ item.name }}&nbsp;</span>
            <span class="">{{ item.value }}</span>
        </div>

    </section>
</template>

<script setup>
let footerList = [
    {name:'آدرس:',value:'محله ناکجا آباد'},
    {name:'شماره تماس:',value:'لورم ای پی ای له ما او'},
]
</script>