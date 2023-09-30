# My Personal Website

[www.keremergur.com](https://www.keremergur.com)

This website was built with 
[Yarn](https://yarnpkg.com/), 
[Vite](https://vitejs.dev/), 
[VueJs](https://vuejs.org/), 
and hosted on 
[Firebase](https://firebase.google.com/).

Icons by 
[Devicon](https://devicon.dev/), 
[Icons8](https://icons8.com/), 
and backgrounds by 
[SVG Backgrounds](https://www.svgbackgrounds.com/).

## Process

I began with a basic vite-vue template for simple scaffolding.

`> yarn create vite`

Initialized both the git repository and the firebase cli.

`> git init`  
`> firebase init`

---

To start, I laid out a basic structure for the website and created each section in 
[`App.vue`](./src/App.vue).

1. Header, Navigation
2. About Me, Links
3. Languages & Tools
4. Interests
5. Projects
6. Footer

Afterwards created the subsections as well. e.g.

- Introduction
- Links

I then created and styled the navbar as a component, and filled in and styled the header.

I created components for repetitive content, one example being 
[`interests`](./src/components/Interest.vue): 

1. Image
2. Title
3. Details

