<template>
	<div class="container">
		<detail-banner
			:sightName="sightName"
			:bannerImg="bannerImg"
			:bannerImages="bannerImages"
		></detail-banner>
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
	},
	data () {
		return {
			sightName: '',
			bannerImg: '',
			bannerImages: []
		}
	},
	methods: {
		getDetailInfo () {
			axios.get('./static/mock/detail.json', {
				params: {
					id: this.$route.params.id
				}
			}).then(this.handleGetDataSucc)
		},
		handleGetDataSucc (res) {
			res = res.data
			if (res.ret && res.data) {
				const data = res.data
				this.sightName = data.sightName
				this.bannerImg = data.bannerImg
				this.bannerImages = data.gallaryImgs
			}
		}
	},
	mounted () {
		this.getDetailInfo()
	}
}
</script>
	
<style lang="stylus" scoped>
	.container
		height: 50rem
</style>