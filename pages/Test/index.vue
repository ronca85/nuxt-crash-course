<template>
	<div>
		<app-parent></app-parent>
	</div>
</template>

<script>
import Parent from '~/components/Parent'

export default {
	name: 'App',
	components: {
		'AppParent': Parent,
	},
	data () {
		return {
		}
	}
}
</script>