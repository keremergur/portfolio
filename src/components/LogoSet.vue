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
  	  	<img :src="addr" height="50" width="50" />
	  </li>
  	</ul>
  </div>
</template>

<style scoped>
ul {
	display: flex;
	justify-content: center;
	width: 15rem;
	padding: 0;
}
li {
	list-style: none;
}
</style>
