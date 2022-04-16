<template>
    <p v-for="(value, key, index, ) in dataList" :key="key">
        {{ index }} : {{ key }} : {{ value }}</p>



</template>

<script setup>
const dataList = {
    a: "John",
    b: "Mary",
    c: "Ken",
    d: "Amy"
};

</script>

<style>
</style>
