<template>
	<div>
		<div class="indicators__left"></div>
		<div class="indicators__right"></div>
		<button class="indicators__button-left">
			<svg class="arrow_left" width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
				<path d="M14.5 12L7 19.5L8.5 21L17.5 12L8.5 3L7 4.5L14.5 12Z" />
			</svg>
		</button>
		<button class="indicators__button-right">
			<svg class="arrow_right" width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
				<path d="M14.5 12L7 19.5L8.5 21L17.5 12L8.5 3L7 4.5L14.5 12Z" />
			</svg>
		</button>
	</div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.indicators {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	pointer-events: none;
	display: flex;
	justify-content: space-between;
	&__left, &__right {
		position: absolute;
		top: 0;
		width: 10%;
		height: 100%;
	}
	&__left {
		background-image: linear-gradient(to left, transparent 25%, #fff 75%);
		left: 0;
	}
	&__right {
		background-image: linear-gradient(to right, transparent 25%, #fff 75%);
		right: 0;
	}
	.arrow_left, .arrow_right {
		background-color: #666;
		pointer-events: auto;
		position: relative;
	}
}
</style>