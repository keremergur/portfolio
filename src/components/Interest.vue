<script setup>
defineProps({
	imgsrc: String,
	title: String,
	info: String
})
</script>

<template>
  <div>
  	<img :src="imgsrc" />
  	<h2>{{ title }}</h2>
  	<p>{{ info }}</p>
  </div>
</template>

<style scoped>
div {
	width: 20rem;
}
</style>
