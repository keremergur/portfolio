<script setup>
defineProps({
    link: String,
    imgsrc: String
});
</script>

<template>
    <li>
        <a :href="link" target="_blank" style="color: white">
            <img :src="imgsrc" />
            <slot></slot>
        </a>
    </li>
</template>

<style scoped>
img {
	height: 2rem; 
	width: 2rem; 
	float: left;
	margin-right: 0.5rem;
	filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
}
</style>