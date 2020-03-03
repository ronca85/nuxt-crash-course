<template>
	<header class="c-header">
		<h1 class="c-title">Dad jokes</h1>
		<ul>
			<li>
				<nuxt-link to="/">Home</nuxt-link>
			</li>
			<li>
				<nuxt-link to="/jokes">Jokes</nuxt-link>
			</li>
			<li>
				<nuxt-link to="/about">About</nuxt-link>
			</li>
		</ul>
	</header>
</template>

<script>
export default {
	name: 'AppHeader',
}
</script>

<style>
.c-header {
	background-color: #fd9;
}
</style>
