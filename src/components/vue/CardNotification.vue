<script setup>
import { ref } from 'vue'
const counter = ref(0)


function decrement() {
    if (counter.value > 0) {
        counter.value--;
    }

}
function increment() {
    counter.value++;
}
</script>

<template>
    <div class="flex-col bg-purple-300 rounded py-8 px-6 w-96 flex items-center ">
        <div class="relative">
            <img class="size-32 rounded-full"
                src="https://files.bo3.gg/uploads/image/36166/image/webp-decbf7bbef7b5ab7e1a0cdb78c1fc3f5.webp" alt="">
            <div v-show="counter > 0"
                class="absolute top-0 right-0 flex justify-center items-center size-6 rounded-full bg-red-400">
                {{ counter }}
            </div>
            

        </div>
        <p v-if="counter > 0 ">Tienes nuevos mensajes!💁‍♀️💁‍♀️</p>
        <p v-else>Nadie te habla😴😴</p>


        <div class="flex justify-around w-24 mt-6">
            <button @click="decrement"
                class="bg-purple-200 rounded w-6 flex justify-center items-center px-2">-</button>
            {{ counter }}
            <button @click="increment"
                class="bg-purple-200 rounded w-6 flex justify-center items-center px-2">+</button>
        </div>
    </div>
</template>