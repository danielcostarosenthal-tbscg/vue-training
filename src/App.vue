// SCRIPT TAG
<script setup>
import Counter from './components/Counter.vue'
const imageSrc = './src/assets/vue.svg'
</script>

// TEMPLATE TAG
<template>
	<div>
		<a href="https://vuejs.org/" target="_blank">
			<img v-bind:src="imageSrc" class="logo vue" alt="Vue logo" />
			<!-- <img :src="imageSrc" class="logo vue" alt="Vue logo" /> -->
		</a>
	</div>

	<Counter msg="Day 1" title="Vue.js Directives" subtitle="Events" />
</template>

// STYLE TAG
<style scoped>
.logo {
	height: 6em;
	padding: 1.5em;
	will-change: filter;
	transition: filter 300ms;
}

.logo.vue:hover {
	filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
