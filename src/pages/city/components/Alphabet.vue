<template>
	<ul class="list">
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
		<li class="item">A</li>
	</ul>
</template>

<script>
export default {
	name: 'CityAlphabet'
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
	.list
		display: flex
		width: .4rem
		flex-direction: column
		justify-content: center
		position: absolute
		top: 1.58rem
		right: 0
		bottom: 0
		.item
			text-align: center
			line-height: .44rem
			color: $bgColor		
</style>