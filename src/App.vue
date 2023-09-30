<script setup>
import Navbar from './components/Navbar.vue';
import LogoSet from './components/LogoSet.vue';
import Interest from './components/Interest.vue';
const introduction = "Munich based student developer at Ludwig-Maximilians-University. Recently, I've mostly used JavaScript, Yarn and Vue.js, always accompanied by Git and sometimes Firebase. You can find my individual skills and interests below.";
const langs = ["https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/haskell/haskell-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"];
const tools = [
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
	"/github.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gitlab/gitlab-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/npm/npm-original-wordmark.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/yarn/yarn-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
	"/vite.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jest/jest-plain.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gradle/gradle-plain.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg",
	"https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-plain.svg"
];
const navstyle = {
	position: "sticky",
	top: "3rem",
	'z-index': 2
};
const navshift = {
	position: 'relative',
	top: '-1rem'
};
</script>

<template>
<div id="container">
  <header>
  	<img id="bghead" src="/bk-prism.svg" />
  	<div id="intro">
	    <div class="greet">
	      <h4>Hey there, I'm</h4>
	      <h1>Kerem Ergür</h1>
	      <h4>a student developer at LMU Munich.</h4>
	    </div>
	    <div>
	      <img id="ppic" src="/ppic.jpg" alt="[Picture]" />
	    </div>
	</div>
  </header>
  <main>
  	<img id="bgmain" src="/liquid.svg" />
  	<div :style="navstyle">
  	  <Navbar :style="navshift" />
  	</div>
  	<section id="about">
  	  <p>{{ introduction }}</p>
  	  <ul>
  	    <li>
    	  <img src="/github.svg" />
     	  <a href="https://github.com/keremergur/"
     	  	target="_blank" style="color: white">GitHub</a>
     	</li>
  	  	<li>
  	  	  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" />
  	  	  <a href="https://linkedin.com/in/keremergur/"
  	  	  	target="_blank" style="color: white">LinkedIn</a>
  	  	</li>
  	  </ul>
  	</section>
  	<section id="skills">
  	  <LogoSet title="Languages" :logos="langs" />
  	  <LogoSet title="Tools" :logos="tools" />
  	</section>
  	<section id="interests">
  	  <h3>Some of my current interests are as follows</h3>
  	  	<div id="imgblocks">
  	  	  <Interest imgsrc="/web.svg" title="Web Development" info="Front-end, REST, CSR/SSR" />
  	  	  <Interest imgsrc="https://img.icons8.com/nolan/256/1A6DFF/C822FF/module.png" title="Software Architecture" info="SOLID, Cohesion" />
  	 	  <Interest imgsrc="https://img.icons8.com/nolan/256/1A6DFF/C822FF/numbered-list.png" title="Database Management" info="SQL, Normalization" />
  	  	  <Interest imgsrc="https://img.icons8.com/nolan/256/1A6DFF/C822FF/share-2.png" title="Computer Networks" info="TCP/IP, DNS, VPN" />
  	  	  <Interest imgsrc="https://img.icons8.com/nolan/256/1A6DFF/C822FF/unlock.png" title="Cybersecurity" info="Cryptography, Ethical Hacking" />
  	  	</div>
  	</section>
  	<section id="projects">
  	<!-- component many -->
  	</section>
  </main>
  <footer>
  </footer>
</div>
</template>

<style scoped>
#container {
	display: grid;
}
header {
	/*background-image: url("./prism.svg");*/
	position: sticky;
	top: -37rem;
	box-shadow: 0 3px 10px rgb(0 0 0 / 1);
	background-color: #111;
	opacity: 100%;
	z-index: 1;
}
#bghead {
	position: absolute;
	top: 0;left: 0;right: 0;bottom: 0;
	width: 100%;height: 100%;
	filter: opacity(50%);
	z-index: -1;
}
#bgmain {
	position: absolute;
	left: 0;right: 0;
	width: 100%;height: 100%;
	object-fit: cover;
	filter: opacity(30%);
	z-index: -3;
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
	filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
}
main {
	position: relative;
}
main section {
	scroll-margin-block-start: 14rem;
}
#about {
	width: 80%;
	display: flex;
	justify-content: space-around;
}
#about p {
	width: 40rem;
	text-align: left;
}
p {
	font-size: 1.2em;
}
#about ul {
	padding: 0;
	width: 10rem;
	font-size: 1.4em;
	display: flex; 
	flex-direction: column; 
	justify-content: space-evenly;
}
#about ul li img {
	height: 2rem; 
	width: 2rem; 
	float: left;
	margin-right: 0.5rem;
	filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
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
#interests {
	width: 80%;
	max-width: 80rem;
}
section {
	margin: 7rem auto;
	z-index: -2;
}
#imgblocks {
	display: flex;
	justify-content: space-evenly;
	flex-wrap: wrap;
}
footer {
	height: 10rem;
	background-color: #161618;
}
</style>
