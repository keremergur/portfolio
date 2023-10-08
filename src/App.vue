<script setup>
import Navbar from './components/Navbar.vue';
import LogoSet from './components/LogoSet.vue';
import Interest from './components/Interest.vue';
import Vlink from './components/Link.vue';

import {introduction,links,languages,tools,interests} from './assets';

const navshift = {
	position: 'relative',
	bottom: '1.3rem'
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
	<div style="height: 0">
  	  <Navbar :style="navshift" />
  	</div>
  </header>
  <main>
  	<img id="bgmain" src="/liquid.svg" />
  	<section id="about">
  	  <p>{{ introduction }}</p>
  	  <ul>
		<vlink v-for="link in links" :link="link.link" :imgsrc="link.imgsrc" >
			{{ link.title }}
		</vlink>
  	  </ul>
  	</section>
  	<section id="skills">
  	  <LogoSet title="Languages" :logos="languages" />
  	  <LogoSet title="Tools" :logos="tools" />
  	</section>
  	<section id="interests">
  	  <h3>Some of my current interests are as follows</h3>
  	  	<div id="imgblocks">
  	  	  <Interest v-for="i in interests"
		  	:imgsrc="i.imgsrc" :title="i.title" :info="i.info" />
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
	top: -35rem;
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
