<template>
	<div>
		<button @click="decrementFontSize()">less</button>
		<h1>Child</h1>
		<button @click="incrementFontSize()">more</button>
	</div>
</template>

<script>
export default {
	name: 'Child',
	data: () => {
		return {
			minFontSize: 1,
			maxFontSize: 3,
		}
	},
	props: {
		fontSize: {
			type: Number,
			default: 1
		},
	},
	methods: {
		decrementFontSize(newFontSize) {
			// console.log("minFontSize", this.minFontSize);
			newFontSize = this.fontSize - 0.25;
			if ( newFontSize < this.minFontSize ) {
				newFontSize = this.minFontSize;
			}
			// console.log("Child - decrement font size via emit to Parent component", newFontSize);
			this.$emit("update:fontSize", newFontSize);
		},
		incrementFontSize(newFontSize) {
			// console.log("maxFontSize", this.maxFontSize);
			newFontSize = this.fontSize + 0.25;
			if ( newFontSize > this.maxFontSize ) {
				newFontSize = this.maxFontSize;
			}
			// console.log("Child - increment font size via emit to Parent component", newFontSize);
			this.$emit("update:fontSize", newFontSize);
		}
	},
}
</script>

<style lang="scss" scoped>
</style>