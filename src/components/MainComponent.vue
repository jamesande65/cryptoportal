<template>
	<div class="main" >
		<div class="container">
			<div class="main_columns">
				<TraidingParisComponent />
				<ContentComponent />
				<AsideComponent />
			</div>
		</div>
	</div>
</template>

<script>
	import TraidingParisComponent from './TradingParisComponent.vue'
	import ContentComponent from './ContentComponent.vue'
	import AsideComponent from './AsideComponent.vue'

	export default {
		components: {
			TraidingParisComponent,
			ContentComponent,
			AsideComponent
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

.main{
	padding: 20px 0 20px;
	scroll-behavior: smooth;
	@include max-screen(640px) {
		padding-bottom: 164px;
	}
	@include max-screen(567px) {
		padding-bottom: 134px;
	}
}

.main_columns{
	display: flex;
	@include max-screen(1440px) {
		flex-wrap: wrap;
	}
	
}

</style>
