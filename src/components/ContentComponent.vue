<template>
	<div class="content">
		<div class="section">
			<div class="section_columns">
				<div class="section_column">
					<TradingGraphComponent />
				</div>
				<div id="subscriptions" class="section_column  second">
					<TradingDealComponent />
				</div>
			</div>
		</div>
		<div class="section" id="top">
			<DealComponent />
		</div>
	</div>
</template>

<script>
	import TradingGraphComponent from './TradingGraphComponent.vue'
	import TradingDealComponent from './TradingDealComponent.vue'
	import DealComponent from './DealComponent.vue'

	export default {
		components: {
			TradingGraphComponent,
			TradingDealComponent,
			DealComponent
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

.content{
	flex-shrink: 1;
	flex-grow: 1;
	min-width: 1px;
	display: flex;
	flex-direction: column;
	@include max-screen(1440px) {
		width: 66.666%;
	}
	@include max-screen(960px) {
		width: 100%;
	}
	.section{
		&:last-child{
			flex-grow: 0;
			flex-shrink: 0;
		}
	}
}
.section_columns{
	display: flex;
	margin: 0 -10px;
	height: 100%;
	flex-direction: column;
	@include max-screen(1280px) {
		flex-direction: column;
		margin: -10px;
	}
}
.section_column{
	padding: 0 10px;
	flex-shrink: 1;
	flex-grow: 1;
	min-width: 1px;
	@include max-screen(1280px) {
		padding: 10px;
	}
	&.second{
		flex-shrink: 0;
		flex-grow: 0;
	}
	.box_aside{
		width: 100%;
	}
}

</style>
