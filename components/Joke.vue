<template>
	<nuxt-link :to="'jokes/' + id">
		<div class="c-joke">
			<p>{{ joke }}</p>
		</div>
	</nuxt-link>
</template>

<script>
export default {
	name: 'Joke',
	props: [ 'joke', 'id' ],
}
</script>

<style>
.c-joke {
	background-color: #e7e7e7;
	padding: 1rem;
	border: dotted 2px #000;
}
</style>
