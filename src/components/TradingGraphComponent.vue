<template>
	<div class="graph" id="trading">
		<div class="graph_panel">
			<div class="item">
				<div class="view positive">
					<i class="icon-arrow-up"></i>
					7.45%
				</div>
			</div>
			<div class="item">
				<span>24H High</span> 11,276.3
			</div>
			<div class="item">
				<span>24H Low</span> 11,250.8
			</div>
			<div class="item">
				<span>24H Volume</span> 100,712.00
			</div>
			<div class="item">
				<em>Current</em> 11,269.10
			</div>
		</div>
		<VueTradingView :options="{
			symbol: 'NASDAQ:AAPL',
			theme: 'dark',
			autosize: true,
			toolbar_bg: '#f1f3f6',
			interval: 'D',
			timezone: 'Etc/UTC',
			style: '1',
			locale: 'en',
			enable_publishing: false,
			allow_symbol_change: true
		}" />
	</div>
</template>

<script>
	import VueTradingView from 'vue-trading-view';
 
	export default {
		name: 'vue-trading-view',
		props: {
			msg: String,
			options: {
				type: [String],
				default: function () {
					return '';
				} 
				// type: [String],
				// required: false,
			}
		},
		// props: {
		// 	options: {
		// 		type: [String],
		// 		default: function () {
		// 			return '';
		// 		} 
		// 		// type: [String],
		// 		// required: false,
		// 	}
		// },
		components: {
			VueTradingView
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

//graph
.graph{
	display: flex;
	flex-direction: column;
	min-height: 100%;
}
.graph_panel{
	display: flex;
	flex-wrap: wrap;
	color: #fff;
	margin: -6px -12px;
	padding-bottom: 14px;
	.item{
		padding: 6px 12px;
	}
	.view{
		color: #788797;
		&.positive{
			color: #56e39e;
		}
		&.negative{
			color: #ff5353;
		}
	}
	span{
		color: #788797;
	}
	em{
		color: #008aff;
	}
}

#vue-trading-view{
	position: relative;
	padding-bottom: 50%;
	@include max-screen(1280px) {
		// min-height: auto;
		padding-bottom: 75%;
	}
	>*{
		position: absolute !important;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		width: 100%;
		height: 100%;
	}
}
</style>