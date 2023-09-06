<script setup>

</script>

<template>
<div>
  <header>
    <div class="greet">
      <h4>Hey there, I'm</h4>
      <h1>Kerem Ergür</h1>
      <h4>a student developer at LMU Munich.</h4>
    </div>
    <div class="photo">
      <p>Image</p>
    </div>
  </header>
  <nav>
  	<li>Intro</li>
  	<li>About</li>
  	<li>Skills</li>
  	<li>Interests</li>
  	<li>Projects</li>
  </nav>
  <main>
  	<p>Brief introduction</p>
  	<aside>Links</aside>
  	<div>Languages and tools</div>
  	<div>Areas of interest with images</div>
  	<div>Projects</div>
  </main>
</div>
</template>

<style scoped>
header {
	height: 20rem;
	display: flex;
	align-items: center;
	justify-content: space-between;
	width: 65%;
	margin: 0 auto;
}
h1 {
	margin: 0;
}
h4 {
	margin: 0;
	padding-top: 1.2rem;
}
nav {
	background-color: darkblue;
	border-radius: 10px;
	width: fit-content;
	margin: 0 auto;
}
nav li {
	display: inline-block;
	list-style: none;
	padding: 0.5rem 1rem;;
	width: 5rem;
}
.greet {
	text-align: left;
}
</style>
