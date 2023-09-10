<script setup>
import Navbar from './components/Navbar.vue';
import LogoSet from './components/LogoSet.vue';
import Interest from './components/Interest.vue';

const links = ["https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg"];
</script>

<template>
<div>
  <header id="intro">
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
  	    <li>
    	  <img />
     	  <a href="https://github.com/keremergur/"
     	  	target="_blank">GitHub</a>
     	</li>
  	  	<li>
  	  	  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" />
  	  	  <a href="https://linkedin.com/in/keremergur/"
  	  	  	target="_blank">LinkedIn</a>
  	  	</li>
  	  </ul>
  	</section>
  	<section id="skills">
  	  <LogoSet title="Languages" :logos="links" />
  	  <LogoSet title="Tools" :logos="[]" />
  	</section>
  	<section id="interests">
  	  <p>Some of my current interests are as follows</p>
  	  	<div id="imgblocks">
  	  	  <Interest title="Web Development" info="Front-end, REST, CSR/SSR" />
  	 	  <Interest title="Database Management" info="SQL, Normalization" />
  	  	  <Interest title="Computer Networks" info="TCP/IP, DNS, VPN" />
  	  	  <Interest title="Cybersecurity" info="Cryptography, Ethical Hacking" />
  	  	</div>
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
main section {
	scroll-margin-block-start: 20rem;
}
#about {
	width: 80%;
	display: flex;
	justify-content: space-between;
}
#about ul {
	padding: 0;
	width: 10rem;
}
#about ul li img {
	height: 1rem;
	width: 1rem;
}
li {
	display: block;
	text-align: left;
}
#skills {
	display: flex;
	justify-content: space-around;
	width: 80%;
}
section {
	margin: 10rem auto;
}
#imgblocks {
	display: flex;
	justify-content: space-evenly;
	flex-wrap: wrap;
}
</style>
