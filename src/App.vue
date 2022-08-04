<template>
	<!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <router-view/>

</template>

<script>

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');
:root {
	--primary: rgba(37, 37, 37, 1);
	--secondary: rgba(252, 41, 74, 1);
	--shades: rgba(238, 238, 238, 1);
}

* {
	scroll-behavior: smooth;
}

body {
	font-family: 'Playfair Display';
	line-height: 1.6;
	margin: 0;
}

.container{
	max-width: 1170px;
    margin-left: auto;
    margin-right: auto;
    padding-left: 16px;
    padding-right: 16px;
}

</style>
