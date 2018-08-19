<template>
	<div>
		<detail-banner></detail-banner>
		<detail-header></detail-header>
	</div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'

import axios from 'axios'
export default {
	name: "Detail",
	components: {
		DetailBanner,
		DetailHeader
	}
}
</script>
	
<style lang="stylus" scoped>
	
</style>