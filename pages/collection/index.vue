<template>
	<div>
		<app-toggle :active.sync="toggleActive" label="Wifi"></app-toggle>
		<app-tabs>
			<app-tab name="tab1" selected="true">content tab 1</app-tab>
			<app-tab name="tab2">content tab 2</app-tab>
			<app-tab name="tab3">content tab 3</app-tab>
			<app-tab name="tab4">content tab 4</app-tab>
			<app-tab name="tab5">content tab 5</app-tab>
			<app-tab name="tab6">content tab 6</app-tab>
			<app-tab name="tab7">content tab 7</app-tab>
			<app-tab name="tab8">content tab 8</app-tab>
			<app-tab name="tab9">content tab 9</app-tab>
		</app-tabs>
	</div>
</template>

<script>
import Toggle from '~/components/Toggle'
import Tabs from '~/components/Tabs'
	import Tab from '~/components/Tab'

export default {
	name: 'App',
	components: {
		'AppToggle': Toggle,
		'AppTabs': Tabs,
		'AppTab': Tab,
	},
	data () {
		return {
			toggleActive: true
		}
	}
}
</script>