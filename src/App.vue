<script setup>
import Navbar from './components/Navbar.vue';
</script>

<template>
<div>
  <header>
    <div class="greet">
      <h4>Hey there, I'm</h4>
      <h1>Kerem Ergür</h1>
      <h4>a student developer at LMU Munich.</h4>
    </div>
    <div>
      <p>Image</p>
    </div>
  </header>
  <Navbar />
  <main>
  	<section id="about">
  	  <p>Brief introduction</p>
  	  <ul>
  	  	<li><a>LinkedIn</a></li>
  	  	<li><a>GitHub</a></li>
  	  </ul>
  	</section>
  	<section id="skills">
  	  <div>
  		<h2>Languages</h2>
  	  </div>
  	  <div>
  	  	<h2>Tools</h2>
  	  </div>
  	  <!-- component (2) -->
  	</section>
  	<section id="interests">
  	<!-- component many -->
  	</section>
  	<section id="projects">
  	<!-- component many -->
  	</section>
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
	margin: 10rem auto;
}
h1 {
	margin: 0;
}
h4 {
	margin: 0;
	padding-top: 1.2rem;
}
.greet {
	text-align: left;
}
#about {
	width: 80%;
	margin: 0 auto;
	display: flex;
	justify-content: space-between;
}
li {
	display: block;
	text-align: left;
}
#skills {
	display: flex;
	justify-content: space-around;
	width: 80%;
	margin: 0 auto;
}
#interests {
	height: 300rem;
}
</style>
