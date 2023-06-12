<script setup lang="ts">
import { defineEmits } from "vue";

const props = defineProps<{ numberValue: string }>();
const emit = defineEmits(["doStuff"]);

function getButtonClicked(value: number) {
	console.log(value);
}
</script>

<template>
	<div class="row">
		<button class="num-button" @click="$emit('doStuff')">1</button>
		<div class="num-button" @click="getButtonClicked(2)">2</div>
		<div class="num-button" @click="getButtonClicked(3)">3</div>
	</div>
	<div class="row">
		<div class="num-button">4</div>
		<div class="num-button">5</div>
		<div class="num-button">6</div>
	</div>
	<div class="row">
		<div class="num-button">7</div>
		<div class="num-button">8</div>
		<div class="num-button">9</div>
	</div>
	<div class="row">
		<div class="num-button">+</div>
		<div class="num-button">-</div>
		<div class="num-button">.</div>
	</div>
	<div class="row">
		<div class="num-button">*</div>
		<div class="num-button">/</div>
		<div class="num-button">=</div>
	</div>
</template>

<style scooped>
.row {
	display: flex;
	justify-content: space-around;
	margin: 10%;
}
.num-button {
	border: 1px solid black;
	text-align: center;
	height: 30px;
	width: 20%;
}
</style>
