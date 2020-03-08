<template>
	<div @click="printUpdatedFontSize()" :style="{ fontSize: fontSize + 'rem' }">
		<TheChild :fontSize.sync="fontSize"></TheChild>
	</div>
</template>

<script>
import Child from '~/components/Child'

export default {
	components: {
		'TheChild': Child,
	},
	data: () => {
		return {
			fontSize: 1
		}
	},
	methods: {
		printUpdatedFontSize() {
			console.log("Parent - font size updated from emit in Child component", this.fontSize);
		}
	},
	created() {
		// console.log("created");
	}
}
</script>

<style lang="scss" scoped>
</style>