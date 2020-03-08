<template>
	<div>
		<app-toggle :active.sync="toggleActive" label="Wifi"></app-toggle>
		<app-tabs>
			<app-tab name="tab1" selected="true">
				content tab 1
			</app-tab>
			<app-tab name="tab2">
				content tab 2
			</app-tab>
			<app-tab name="tab3">
				content tab 3
			</app-tab>
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