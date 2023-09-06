<script setup>

</script>

<template>
  <nav>
	<li>Intro</li>
	<li>About</li>
	<li>Skills</li>
	<li>Interests</li>
	<li>Projects</li>
  </nav>
</template>

<style scoped>
nav {
	background-color: azure;
	border-radius: 10px;
	width: fit-content;
	margin: 0 auto;
}
nav li {
	color: black;
	display: inline-block;
	list-style: none;
	padding: 0.5rem 1rem;;
	width: 5rem;
}
nav li:hover {
	background-color: cyan;
}
</style>
