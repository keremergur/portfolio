<script setup>
import Navbar from './components/Navbar.vue';
import LogoSet from './components/LogoSet.vue';
import Interest from './components/Interest.vue';

const links = ["https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/haskell/haskell-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"];
const tools = [
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gitlab/gitlab-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/npm/npm-original-wordmark.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/yarn/yarn-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gradle/gradle-plain.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg"
];
const navstyle = {
	position: "sticky",
	top: "3rem"
};
const navshift = {
	position: 'relative',
	top: '-1rem'
};
</script>

<template>
<div id="container">
  <header>
  	<div id="intro">
	    <div class="greet">
	      <h4>Hey there, I'm</h4>
	      <h1>Kerem Ergür</h1>
	      <h4>a student developer at LMU Munich.</h4>
	    </div>
	    <div>
	      <img id="ppic" src="./ppic.jpg" alt="[Picture]" />
	    </div>
	</div>
  </header>
  <div :style="navstyle">
  	<Navbar :style="navshift" />
  </div>
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
  	  <LogoSet title="Tools" :logos="tools" />
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
#container {
	display: grid;
}
header {
	background-image: url("./prism.svg");
}
#intro {
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
#ppic {
	height: 22rem;
	border-radius: 30px;
}
main section {
	scroll-margin-block-start: 14rem;
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
