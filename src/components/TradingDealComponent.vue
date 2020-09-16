<template>
	<div class="box_aside" id="tabs_aside">
		<div class="box_content content_open is_open" data-tab-content="1">
			<form action="#">
				<div class="row">
					<div class="box_sup">
						<em>Доступный баланс</em>
						<ul class="list">
							<li class="item">
								<span><strong>24</strong> LTC</span>
							</li>
							<li class="item">
								<span><strong>0.5</strong> BTC</span>
							</li>
						</ul>
					</div>
				</div>
				<div class="row">
					<div class="panel_choice">
						<div class="btn_choice">
							<input type="radio" id="radio_choice1" name="radio1" class="field_radio" checked>
							<label for="radio_choice1" class="label_radio">LIMIT</label>
						</div>
						<div class="btn_choice">
							<input type="radio" id="radio_choice2" name="radio1" class="field_radio">
							<label for="radio_choice2" class="label_radio">MARKET</label>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="box_second">
						<div class="sep">
							<div class="columns">
								<div class="col">
									<label for="#" class="label">Цена покупки</label>
								</div>
								<div class="col second">
									<input type="text" class="input single" value="0.00000001">
								</div>
							</div>
						</div>
						<div class="sep">
							- или -
						</div>
						<div class="sep">
							<div class="columns">
								<div class="col">
									<label for="#" class="label">% от депозита</label>
								</div>
								<div class="col second">
									<input type="text" class="input single" value="2,5%">
								</div>
							</div>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="columns">
						<div class="col">
							<label for="#" class="label">Количество BTC</label>
						</div>
						<div class="col second">
							<input type="text" class="input single" value="0.00000001">
						</div>
					</div>
				</div>
				<div class="row">
					<div class="droppped_box">
						<button type="button" class="btn_more">
							<span>Advanced</span>
							<i class="icon-arrow-drop-down"></i>
						</button>
						<div class="hidden_block">
							<div class="row">
								<div class="columns">
									<div class="col">
										<label for="#" class="label">Stop loss, %</label>
									</div>
									<div class="col second">
										<input type="text" class="input single" value="2.6%">
									</div>
								</div>
							</div>
							<div class="row">
								<div class="columns">
									<div class="col">
										<label for="#" class="label">Take profit</label>
									</div>
									<div class="col second">
										<input type="text" class="input single" value="2.6%">
									</div>
								</div>
							</div>
							<div class="row">
								<div class="columns">
									<div class="col">
										<label for="#" class="label"><span>Наценка</span></label>
									</div>
									<div class="col second">
										<input type="text" class="input single" value="2.6">
									</div>
								</div>
							</div>
							<div class="row">
								<div class="columns">
									<div class="col">
										<label for="#" class="label"><span>Кол-во</span></label>
									</div>
									<div class="col second">
										<input type="text" class="input single" value="5">
									</div>
								</div>
							</div>
							<div class="row">
								<div class="columns">
									<div class="col">
										<label for="#" class="label"><span>Stop loss,%</span></label>
									</div>
									<div class="col second">
										<input type="text" class="input single" value="2.6%">
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div class="row">
					<input type="checkbox" id="checkbox1" class="field_checkbox">
					<label for="checkbox1" class="label_checkbox">Опубликовать сделку для платных подписчиков</label>
				</div>
				<div class="row">
					<input type="checkbox" id="checkbox2" class="field_checkbox">
					<label for="checkbox2" class="label_checkbox">Опубликовать сделку для бесплатных подписчиков
						<i class="icon-question">
							<span class="tooltip">Etiam vel turpis vitae tortor pellentesque tristique. Integer sagittis aliquet odio non tincidunt.</span>
						</i>
					</label>
				</div>
			</form>
		</div>
		<div class="box_content content_open" data-tab-content="2">
			<form action="#">
				<div class="row">
					<div class="box_sup">
						<em>Доступный баланс</em>
						<ul class="list">
							<li class="item">
								<span><strong>42</strong> LTC</span>
							</li>
							<li class="item">
								<span><strong>1.5</strong> BTC</span>
							</li>
						</ul>
					</div>
				</div>
				<div class="row">
					<div class="panel_choice">
						<div class="btn_choice">
							<input type="radio" id="radio_choice3" name="radio2" class="field_radio" checked>
							<label for="radio_choice3" class="label_radio">LIMIT</label>
						</div>
						<div class="btn_choice">
							<input type="radio" id="radio_choice4" name="radio2" class="field_radio">
							<label for="radio_choice4" class="label_radio">MARKET</label>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="box_second">
						<div class="sep">
							<div class="columns">
								<div class="col">
									<label for="#" class="label">Цена покупки</label>
								</div>
								<div class="col second">
									<input type="text" class="input single" value="0.00000001">
								</div>
							</div>
						</div>
						<div class="sep">
							- или -
						</div>
						<div class="sep">
							<div class="columns">
								<div class="col">
									<label for="#" class="label">% от депозита</label>
								</div>
								<div class="col second">
									<input type="text" class="input single" value="2,5%">
								</div>
							</div>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="columns">
						<div class="col">
							<label for="#" class="label">Количество BTC</label>
						</div>
						<div class="col second">
							<input type="text" class="input single" value="0.00000001">
						</div>
					</div>
				</div>
				<div class="row">
					<input type="checkbox" id="checkbox3" class="field_checkbox">
					<label for="checkbox3" class="label_checkbox">Опубликовать сделку для платных подписчиков</label>
				</div>
				<div class="row">
					<input type="checkbox" id="checkbox4" class="field_checkbox">
					<label for="checkbox4" class="label_checkbox">Опубликовать сделку для бесплатных подписчиков</label>
				</div>
			</form>
		</div>
		<div class="box_heading">
			<div class="item_tab positive onTab is_active" data-tab-trigger="1">Buy</div>
			<div class="item_tab negative onTab" data-tab-trigger="2">Sell</div>
		</div>
	</div>
</template>

<script>
	export default {
		mounted() {
			tabsBox();
			dropSection();
		}
	}
	function tabsBox() {
		var tabTriggerBtns = document.querySelectorAll('.onTab');

		tabTriggerBtns.forEach(function (tabTriggerBtn) {
			tabTriggerBtn.addEventListener('click', function () {
				var currentTabData = document.querySelector('.content_open[data-tab-content="' + this.dataset.tabTrigger + '"]');

				// remove classess
				document.querySelector('.content_open.is_open').classList.remove('is_open');
				document.querySelector('.onTab.is_active').classList.remove('is_active');
				// add classes
				currentTabData.classList.add('is_open');
				this.classList.add('is_active');
			});
		});
	}
	function dropSection() {
		const obj = document.querySelector('.btn_more');
		obj.onclick = function () {
			obj.parentElement.classList.toggle('active');
		}
	}
</script>

<style lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";


.box_heading{
	display: flex;
	background-color: #37434f;
}
.item_tab{
	width: 50%;
	padding: 14px;
	text-align: center;
	color: #fff;
	transition: color .3s;
	font-size: 14px;
	cursor: pointer;
	font-weight: 500;
	letter-spacing: 0.6px;
	text-transform: uppercase;
	position: relative;
	@include min-screen(1025px) {
		&:hover{
			color: #008aff;
		}
	}
	@include max-screen(640px) {
		margin: 2px;
		&.positive{
			background-color: #42c685;
			&.is_active{
				color: #fff;
				&:after{
					display: none;
				}
			}
		}
		&.negative{
			background-color: #f62650;
			&.is_active{
				color: #fff;
				&:after{
					display: none;
				}
			}
		}
	}
	&.is_active{
		color: #008aff;
		&:after{
			display: block;
		}
	}
	&:after{
		content: "";
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		height: 2px;
		background-color: #008aff;
		display: none;
	}
}
.box_content{
	padding: 20px;
	// display: none;
	// &.active{
	// 	display: block;
	// }
	.row{
		margin-bottom: 15px;
		&:last-child{
			margin-bottom: 0;
		}
	}
	.columns{
		display: flex;
		align-items: center;
	}
	.col{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 10px;
		&.second{
			flex-shrink: 1;
			flex-grow: 1;
			min-width: 1px;
			max-width: 134px;
			width: 100%;
			margin: 0 0 0 auto;
		}
	}
	.label{
		color: #fff;
		font-family: 'Roboto', sans-serif;
		font-size: 14px;
		font-weight: 400;
		letter-spacing: 0.2px;
		text-transform: none;
		span{
			color: #9faab7;
		}
	}
	.input{
		text-align: right;
	}
	// .btn{
	// 	border-radius: 8px;
	// 	padding: 14px 22px;
	// 	color: #fff;
	// 	font-family: 'Roboto', sans-serif;
	// 	font-size: 14px;
	// 	font-weight: 500;
	// 	letter-spacing: 0.6px;
	// 	border: none;
	// 	cursor: pointer;
	// 	text-transform: uppercase;
	// 	color: #fff;
	// 	background-color: #42c685;
	// }
}
.content_open{
	display: none;
	&.is_open{
		display: block;
	}
}
.box_sup{
	display: flex;
	font-size: 12px;
	color: #bac9dd;
	align-items: center;
	em{
		margin-right: 10px;
		flex-shrink: 0;
		flex-grow: 0;
	}
	.list{
		display: flex;
		justify-content: flex-end;
		margin: 0 -15px;
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
	}
	.item{
		padding: 0 15px;
		position: relative;
		&:before{
			content: "";
			position: absolute;
			top: 0;
			left: 0;
			bottom: 0;
			background-color: #303c5d;
			width: 1px;
		}
		&:first-child{
			&:before{
				display: none;
			}
		}
	}
	span{
		color: #fff;
		font-size: 18px;
		text-transform: uppercase;
	}
}
.panel_choice{
	border-radius: 8px;
	overflow: hidden;
	background-color: #37434f;	
	display: flex;
}
.btn_choice{
	width: 50%;
	.field_radio{
		display: none;
		&:checked + .label_radio{
			background-color: #008aff;
		}
	}
	.label_radio{
		display: block;
		text-align: center;
		padding: 8px;
		cursor: pointer;
		color: #fff;
		font-family: 'Roboto', sans-serif;
		font-size: 12px;
		font-weight: 500;
		letter-spacing: 0.51px;
		text-transform: uppercase;
	}
}
.box_second{
	background-color: #2e3842;
	margin: 0 -20px;
	padding: 15px 20px;
	.sep{
		margin-bottom: 8px;
		font-weight: 700;
		letter-spacing: 0.2px;
		text-transform: uppercase;
		text-align: center;
		&:last-child{
			margin-bottom: 0;
		}
	}
}
.field_checkbox{
	display: none;
	&:checked + .label_checkbox{
		&:before{
			background-color: #008aff;
			border-color: #008aff;
		}
		&:after{
			opacity: 1;
		}
	}
}
.icon-question{
	position: relative;
	&:hover{
		&:after{
			display: block;
		}
		.tooltip{
			display: block;
		}
	}
	&:after{
		content: "";
		position: absolute;
		bottom: 20px;
		right: 2px;
		width: 0;
		height: 0;
		border-left: 5px solid transparent;
		border-right: 5px solid transparent;
		border-top: 6px solid #788797;
		display: none;
	}
}
.tooltip{
	position:absolute;
	bottom: calc(100% + 11px);
	right: -45px;
	border-radius: 8px;
	background-color: #788797;
	padding: 10px 15px;
	color: #fff;
	font-size: 12px;
	font-weight: 500;
	line-height: 1.4;
	font-family: 'Roboto', sans-serif;
	letter-spacing: 0.17px;
	display:none;
	width: 195px;
}
.label_checkbox{
	position: relative;
	color: #fdfdfd;
	font-family: 'Roboto', sans-serif;
	font-size: 14px;
	font-weight: 400;
	letter-spacing: 0.2px;
	padding-left: 28px;
	display: inline-block;
	vertical-align: top;
	&:before{
		content: "";
		position: absolute;
		top: 0;
		left: 0;
		width: 18px;
		height: 18px;
		border-radius: 3px;
		border: 1px solid #748392;
	}
	&:after{
		content: "";
		position: absolute;
		top: 5px;
		left: 4px;
		border: 2px solid #fff;
		border-top: none;
		border-right: none;
		width: 10px;
		height: 6px;
		transform: rotate(-45deg);
		opacity: 0;
		transition: opacity .3s;
	}
	i{
		cursor: pointer;
		font-size: 14px;
		vertical-align: bottom;
		color: #008aff;
	}
}
.droppped_box{
	&.active{
		.btn_more{
			i{
				transform: rotate(180deg);
			}
		}
		.hidden_block{
			display: block;
		}
	}
}
.hidden_block{
	display: none;
}
.btn_more{
	background: none;
	border: none;
	color: #bfcefb;
	font-family: 'Roboto', sans-serif;
	font-size: 16px;
	font-weight: 700;
	display: flex;
	align-items: center;
	letter-spacing: 0.6px;
	cursor: pointer;
	margin-bottom: 20px;
	span{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 5px;
	}
	i{
		flex-shrink: 0;
		flex-grow: 0;
	}
}
</style>