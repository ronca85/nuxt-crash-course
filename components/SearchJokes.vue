<template>
	<form @submit.prevent="onSubmit">
		<input type="text" v-model="text" placeholder="Search Jokes...">
		<button type="submit">Search Jokes</button>
	</form>
</template>

<script>
export default {
	name: 'SearchJokes',
	data() {
		return {
			text: '',
		}
	},
	methods: {
		onSubmit() {
			this.$emit('search-text', this.text); // this.text becomes emittedText parameter in searchText function in the Jokes Page
			this.text = "";
		}
	}
}
</script>

<style>
.c-joke {
	background-color: #e7e7e7;
	padding: 1rem;
	border: dotted 2px #000;
}
</style>
