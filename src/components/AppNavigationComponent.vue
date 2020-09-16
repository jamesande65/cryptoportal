<template>
	<div class="app_navigation">
		<div class="columns">
			<div class="column second">
				<a class="item" href="#trading">
					<i class="icon-stat"></i>
					<span>Трейдинг</span>
				</a>
				<a class="item" href="#top">
					<i class="icon-star-top"></i>
					<span>Топы</span>
				</a>
				<a class="item active" href="#exchanges">
					<i class="icon-around"></i>
					<span>Биржи</span>
				</a>
			</div>
			<div class="column">
				<div class="item">
					<div class="wrap_button">
						<a href="#" class="button">
							<i class="icon-arrows"></i>
						</a>
					</div>
				</div>
			</div>
			<div class="column second">
				<a class="item" href="#subscriptions">
					<i class="icon-port"></i>
					<span>Подписки</span>
				</a>
				<a class="item" href="#balance">
					<i class="icon-notes"></i>
					<span>Баланс</span>
				</a>
				<a class="item" href="#chat">
					<i class="icon-chat"></i>
					<span>Чат</span>
				</a>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	
}
</script>

<style scoped lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

.app_navigation{
	position: fixed;
	bottom: 0;
	left: 0;
	right: 0;
	z-index: 998;
	font-size: 13px;
	display: none;
	transform: translate3d(0, 0, 0);
	opacity: 1;
	visibility: visible;
	transition: transform .6s, opacity .6s, visibility .6s;
	// @include max-screen(1024px) {
	// 	display: block;
	// }
	@include max-screen(640px) {
		display: block;
	}
	@include max-screen(567px) {
		font-size: 11px;
	}
	&:after{
		content: "";
		position: absolute;
		bottom: 0;
		left: 50%;
		transform: translate3d(-50%, 0, 0);
		// right: 0;
		background: url("../images/bg.svg") no-repeat;
		// width: 100%;
		width: 640px;
		// height: 100%;
		height: 90px;
		margin: 0 auto;
		background-position: calc(50% - 3px) center;
		@include max-screen(567px) {
			height: 68px;
		}
		@include max-screen(374px) {
			background-position: calc(50% + 1px) center;
		}
	}
	.columns{
		display: flex;
		justify-content: space-between;
		position: relative;
		&:before{
			content: "";
			position: absolute;
			bottom: 0;
			top: 0;
			left: -50%;
			width: 100%;
			box-shadow: 0 -5px 10px rgba(0, 0, 0, 0.15);
			transform: translateX(-15%);
			background-image: linear-gradient(180deg, #303b4d 0%, #202a34 100%);
		}
		&:after{
			content: "";
			position: absolute;
			bottom: 0;
			top: 0;
			right: -50%;
			width: 100%;
			box-shadow: 0 -5px 10px rgba(0, 0, 0, 0.15);
			transform: translateX(15%);
			background-image: linear-gradient(180deg, #303b4d 0%, #202a34 100%);
		}
	}
	.column{
		flex-shrink: 0;
		flex-grow: 0;
		display: flex;
		position: relative;
		z-index: 2;
		&.second{
			flex-shrink: 1;
			flex-grow: 1;
			min-width: 1px;
		}
	}
	.item{
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
		position: relative;
		&:before{
			content: "";
			position: absolute;
			top: 0;
			left: 0;
			right: 0;
			bottom: 0;
			width: 100%;
			height: 100%;
		}
		&.active{
			color: #fff;
			i{
				color: #008aff;
			}
		}
	}
	a{
		color: #8999a9;
		display: flex;
		align-items: center;
		flex-direction: column;
		padding: 15px;
		@include max-screen(567px) {
			padding: 10px;
		}
	}
	.wrap_button{
		position: relative;
		top: -50px;
		@include max-screen(567px) {
			top: -40px;
		}
	}
	.button{
		width: 80px;
		height: 80px;
		color: #fff;
		transform-origin: center;
		transform: rotate(-315deg);
		box-shadow: 0 0 20px rgba(31, 146, 244, 0.45);
		border-radius: 25px;
		background-image: linear-gradient(180deg, #008aff 0%, #0074dd 100%);
		@include max-screen(567px) {
			width: 60px;
			height: 60px;
			border-radius: 20px;
		}
		i{
			font-size: 33px;
			transform: translate3d(-50%, -50%, 0) rotate(315deg);
			position: absolute;
			top: 50%;
			left: 50%;
			@include max-screen(567px) {
				font-size: 28px;
			}
		}
	}
	i{
		font-size: 35px;
		@include max-screen(567px) {
			font-size: 25px;
		}
		@include max-screen(374px) {
			font-size: 20px;
		}
	}
	span{
		margin-top: 10px;
	}
}
</style>