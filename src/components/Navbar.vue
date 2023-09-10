<script setup>

</script>

<template>
  <nav>
	<li><a href="#">Intro</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#skills">Skills</a></li>
	<li><a href="#interests">Interests</a></li>
	<li><a href="#">Projects</a></li>
  </nav>
</template>

<style scoped>
nav {
	background-color: azure;
	border-radius: 10px;
	width: fit-content;
	margin: 0 auto;
	position: sticky;
	top: 2rem;
	box-shadow: 0 3px 10px rgb(0 0 0 / 1);
}
nav li {
	color: black;
	display: inline-block;
	list-style: none;
}
nav li:hover {
	background-color: cyan;
}
a {
	display: inline-block;
	padding: 0.5rem 1rem;
	width: 5rem;
	
}
</style>
