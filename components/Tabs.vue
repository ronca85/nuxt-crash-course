<template>
	<article class="tabs">
		<header class="tabs__header">
			<ul class="tabs__list">
				<li class="tabs__item" v-for="(tab, index) in tabs" :key="index">
					<div class="nav-item"
						:class="{ 'is-active' : tab.isActive }"
						@click="handleTabSelect(tab)"
					>
						{{ tab.name }}
					</div>
				</li>
			</ul>
			<TheIndicators v-if="indicators" class="indicators"></TheIndicators>
		</header>
		<section class="tabs__body">
			<slot></slot>
		</section>
	</article>
</template>

<script>
import Indicators from '~/components/Indicators'

export default {
	components: {
		'TheIndicators': Indicators,
	},
	data: () => {
		return {
			indicators: true,
			tabs: [],
		}
	},
	methods: {
		handleTabSelect(selectedTab) {
			this.tabs.forEach( tab => {
				tab.isActive = tab.name === selectedTab.name;
				// note: if two tabs have the same name this will not work
			});
		}
	},
	created() {
		// console.log("tabs this", this);
		this.tabs = this.$children;
	}
}
</script>

<style lang="scss" scoped>
.tabs {
	&__header {
		position: relative;
	}
	&__list {
		list-style: none;
		padding: 0;
		display: flex;
		overflow-x: auto;
		white-space: nowrap;
		user-select: none;
		-webkit-overflow-scrolling: touch;
		-ms-overflow-style: -ms-autohiding-scrollbar; 
		&::-webkit-scrollbar {
			display: none;
		}
	}
	&__item {
		flex: 1 0 60%;
	}
}
.nav-item {
	text-align: center;
	border: 2px dashed #aaa;
	cursor: pointer;
	&:hover {
		background-color: #aaa;
		border: 2px dashed #666;
	}
	&:active {
		background-color: #666;
		border: 2px dashed #333;
		color: #fff;
	}
	&.is-active {
		background-color: #adf;
		border: 2px dashed #36a;
		color: #333;
	}
}
</style>