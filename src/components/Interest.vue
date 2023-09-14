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
	margin: 2rem;
}
img {
	height: 10rem;
	width: 10rem;
	filter: opacity(75%);
}
h2 {
	margin: 0 auto;
}
</style>
