<template>
    <p class="text-animation" :key="text">{{ text }}</p>
    <!-- <p v-for="(value, key, index, ) in dataList" :key="key">
     <span v-show="value !== 'c'"> {{ index }} : {{ key }} : {{ value }}</span> 
    </p> -->




</template>

<script setup>
import { ref } from 'vue';
const text = ref("title");

const dataList = {
    a: "John",
    b: "Mary",
    c: "Ken",
    d: "Amy",
    e: "Sam"
};

const dataArray = [
    "orange", "apple", "banana"
];



let index = 0;
setInterval(() => {

    if (index < dataArray.length) {
        text.value = dataArray[index];
        index += 1;
    } else {
        index = 0
    }

}, 1500)




</script>

<style>
.text-animation {
    font-size: 32px;
    animation: openIn 1s ease-in-out;
}

@keyframes openIn {
    0% {
        opacity: 0;
        transform: translateY(20px);
    }

    100% {
        opacity: 1;
        transform: translateY(0px);
    }
}
</style>
