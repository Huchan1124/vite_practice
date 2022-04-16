<template>

	<button @click="showView(1)">{{ title1 }}</button>
	<button @click="showView(2)">{{ title2 }}</button>
	<br>
	<div class="container1" v-if="view === 1">
		<h3>{{ title1 }}</h3>
		<p>Hello World!</p>
	</div>
	<div class="container2" v-else-if="view === 2">
		<h3>{{ title2 }}</h3>
		<input type="text" v-model="text">
		<p>{{ text }}</p>
	</div>
	<div class="container3" v-else>
		<p>沒有東西</p>
	</div>

</template>

<script setup>
import { ref } from 'vue';

const title1 = '資料綁定:單向綁定';
const title2 = '資料綁定:雙向綁定';
const text = ref('123');
const view = ref(0);

const showView = (index) => {
	view.value = index;
}


</script>

<style>
.container1 {
	border: 2px solid red;
}

.container2 {
	border: 2px solid blue;
}
</style>
