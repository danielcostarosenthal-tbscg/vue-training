// SCRIPT TAG
<script setup>
import { ref } from 'vue'

// PROPS
defineProps({
	msg: String,
	title: String,
	subtitle: String,
})

// Counter state
const count = ref(0)

// Visibility state
const isVisible = ref(true)

const toggleVisibility = () => {
	isVisible.value = !isVisible.value
}
</script>

// TEMPLATE TAG
<template>
	<!-- DIRECTIVES -->
	<h1>{{ msg }}</h1>
	<h3>{{ title }}</h3>
	<p v-if="true">Paragraph is visible <code class="code">v-if="true"</code></p>
	<p v-if="isVisible">Paragraph is visible</p>

	<!-- ON CLICK EVENTS -->
	<h3>{{ subtitle }}</h3>
	<div class="card">
		<button class="btn" type="button" @click="count++">count is {{ count }}</button>
	</div>
	<div class="card">
		<button class="btn" @click="toggleVisibility">Toggle Visibility</button>
		<p class="visibility" v-show="isVisible">I am visible</p>
	</div>
</template>

// STYLE TAG
<style scoped>
.code,
.btn {
	padding: 4px 8px;

	background-color: #41b883;
	border-radius: 2px;
	color: #fff;
}

button {
	outline: none;
	border: none;
}
</style>
