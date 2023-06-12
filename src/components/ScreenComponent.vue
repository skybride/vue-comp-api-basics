<script setup lang="ts">
defineProps<{ displayValue: string }>();
</script>

<template>
	<div class="container">{{ displayValue }}</div>
</template>

<style scoped>
.container {
	border: 2px solid lightslategray;
	height: 80px;
	margin: 4% 10% 0 10%;
	font-size: 40px;
	padding-left: 4%;
}
</style>
