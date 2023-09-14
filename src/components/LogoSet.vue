<script setup>
defineProps({
	title: String,
	logos: [String]
});
</script>

<template>
  <div>
  	<h2>{{ title }}</h2>
  	<ul>
  	  <li v-for="addr in logos" :id="addr">
  	  	<img :src="addr" />
	  </li>
  	</ul>
  </div>
</template>

<style scoped>
ul {
	display: flex;
	justify-content: center;
	flex-wrap: wrap;
	width: 25rem;
	padding: 0;
}
li {
	list-style: none;
	margin: 0.5rem;
}
img {
	height: 4rem;
	width: 4rem;
	filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
}
</style>
