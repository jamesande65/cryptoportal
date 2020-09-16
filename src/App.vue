<template>
	<div id="app" class="wrapper">
		<HeaderComponent/>
		<MainComponent/>
		<AppNavigationComponent/>
		<FooterComponent/>
	</div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import AppNavigationComponent from './components/AppNavigationComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
	name: 'App',
	components: {
		HeaderComponent,
		MainComponent,
		AppNavigationComponent,
		FooterComponent
	}
}
</script>

<style lang="scss">
@import "styles/variables";
@import "styles/mixins";
@import "styles/media-queries";
@import "styles/res";

@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,300;0,400;0,700;1,900&display=swap');
@include font-face('Ico Moon', './fonts/icomoon', normal, normal);

html{
	height:100%;
	min-width:320px;
	-webkit-text-size-adjust: 100%;
	-ms-text-size-adjust: 100%;
}
#app,
body{
	font: 14px/1.2 'Open Sans', Helvetica, sans-serif;
	height: 100%;
	min-width:320px;
	position:relative;
	color:#fff;
	background:#1e252e;
	&.open{
		position: fixed;
		overflow: hidden;
		.app_navigation{
			opacity: 0;
			visibility: hidden;
			transform: translate3d(0, 100%, 0);
		}
	}
}
a{
	color:#2600ff;
	text-decoration:none;
}
input{
	outline:none;
	-webkit-appearance:none;
	-webkit-border-radius:0;
	-moz-border-radius:0;
	border-radius:0;
}
*{
	outline: none;
}
* {
	box-sizing: border-box;
	&:before, &:after{
		box-sizing: border-box;
	}
}

.wrapper{
	display: table;
	width: 100%;
	height: 100%;
	table-layout: fixed;
	overflow: hidden;
	position: relative;
}


.container{
	padding: 0 20px;
	@include max-screen(479px) {
		padding: 0 10px;
	}
}

.section{
	margin-bottom: 22px;
	flex-shrink: 1;
	flex-grow: 1;
	min-height: 1px;
	position: relative;
	&:last-child{
		margin-bottom: 0;
	}
	&.last{
		flex-shrink: 0;
		flex-grow: 0;
	}
}

//aside
.aside{
	flex-shrink: 0;
	flex-grow: 0;
	// margin: 0 20px 0 0;
	padding: 0 20px 0 0;
	display: flex;
	flex-direction: column;
	@include max-screen(1440px) {
		// width: 300px;
		width: 33.333%;
	}
	@include max-screen(960px) {
		width: 100%;
		margin: 0 0 20px;
		padding: 0;
	}
}
.box_aside{
	background-color: #232d38;
	width: 330px;
	height: 100%;
	display: flex;
	flex-direction: column;
	@include max-screen(1440px) {
		width: 100%;
	}
	form{
		height: 100%;
	}
	.wrap{
		display: flex;
		flex-direction: column;
		height: 100%;
	}
	.heading{
		background-color: #253443;
		padding: 12px 15px;
		display: flex;
		align-items: center;
		flex-shrink: 0;
		flex-grow: 0;
		.custom-select{
			margin-left: 15px;
		}
	}
	.title{
		font-size: 15px;
		font-weight: 700;
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
	}
	.wraped{
		position: relative;
		height: 100%;
		width: 100%;
	}
}

//custom scroll
.scrollscreen	{
	position: relative;
}

.scrollscreen--track {
	position: absolute;
	right: 6px;
	top: 0;
	height: 100%;
	pointer-events: none;
}

*[dir='rtl'] .scrollscreen--track {
	left: 0;
	right: auto;
}

.scrollscreen--slider {
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	box-sizing: border-box;
	height: 0;
	border: none;
	background: transparent;
	pointer-events: none;
}

.scrollscreen--slider::after {
	content: '';
	display: block;
	width: 100%;
	height: 100%;
}

.scrollscreen--content {
	position: relative;
	height:100%;
	overflow-x: hidden;
	overflow-y: auto;
}

.scrollscreen--content::-webkit-scrollbar {
    /* fix WebKit problems with MacOS automatically hiding scrollbars */
    -webkit-appearance: none;
}
.scrollscreen--track {
    /* width of track, 18px should cover default track on MacOS and Windows */
    width: 4px;
	background: transparent;
	border-radius: 3px;
}
.scrollscreen--slider::after {
	background-color: #8999a9;
    border-radius:9999em;
}

//icon
[class^="icon-"], [class*=" icon-"] {
	/* use !important to prevent issues with browser extensions that change fonts */
	font-family: 'Ico Moon' !important;
	font-size: 12px;
	speak: none;
	font-style: normal;
	font-weight: normal;
	font-variant: normal;
	text-transform: none;
	line-height: 1;

	/* Better Font Rendering =========== */
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}
.icon-settings:before {
  content: "\e91b";
}
.icon-chat-fill:before {
  content: "\e91c";
}
.icon-menu:before {
  content: "\e91d";
}
.icon-papper:before {
  content: "\e91e";
}
.icon-statistic:before {
  content: "\e91f";
}
.icon-question:before {
  content: "\e918";
}
.icon-around:before {
  content: "\e911";
}
.icon-arrows:before {
  content: "\e912";
}
.icon-chat:before {
  content: "\e913";
}
.icon-notes:before {
  content: "\e914";
}
.icon-port:before {
  content: "\e915";
}
.icon-star-top:before {
  content: "\e916";
}
.icon-stat:before {
  content: "\e917";
}
.icon-play:before {
  content: "\e910";
}
.icon-arrow-right:before {
  content: "\e90f";
}
.icon-messager:before {
  content: "\e90a";
}
.icon-phone:before {
  content: "\e90b";
}
.icon-skype:before {
  content: "\e90c";
}
.icon-telegram:before {
  content: "\e90d";
}
.icon-viber:before {
  content: "\e90e";
}
.icon-cash:before {
  content: "\e909";
}
.icon-circle-accept:before {
  content: "\e908";
}
.icon-n-smile:before {
  content: "\e904";
}
.icon-target:before {
  content: "\e905";
}
.icon-up-statistic:before {
  content: "\e906";
}
.icon-hands:before {
  content: "\e907";
}
.icon-logout:before {
  content: "\e903";
}
.icon-arrow-up:before {
  content: "\e901";
}
.icon-bell:before {
  content: "\e902";
}
.icon-search:before {
  content: "\e91a";
}
.icon-arrow-drop-down:before {
  content: "\e900";
}
.icon-close:before {
  content: "\e920";
}
.icon-send:before {
  content: "\e919";
}

//custom select
.custom-select {
	position: relative;
	font-family: 'Roboto', sans-serif;
	width: 100%;
	select {
		display: none; 
	}
}
.select-selected {
	background-color: #232d38;
	white-space: nowrap;
	overflow: hidden;
	text-overflow: ellipsis;
	&:before{
		position: absolute;
		content: "";
		top: 0;
		right: 0;
		width: 24px;
		height: 100%;
		border-left: 1px solid #37434f;
	}
	&:after {
		position: absolute;
		content: "";
		top: 16px;
		right: 7px;
		width: 0;
		height: 0;
		border: 5px solid transparent;
		border-color: #788797 transparent transparent transparent;
	}
	&.select-arrow-active{
		&:after {
			border-color: transparent transparent #fff transparent;
			top: 10px;
		}
	}
}
.select-items div,
.select-selected {
	color: #fff;
	padding: 9px 24px 9px 16px;
	cursor: pointer;
	user-select: none;
}
.select-selected{
	color: #788797;
	height: 36px;
	overflow: hidden;
	border-radius: 7px;
	border: 1px solid #37434f;
	&.select-arrow-active{
		border-radius: 7px 7px 0 0;
	}
}
.select-items {
	position: absolute;
	background-color: #232d38;
	top: 100%;
	left: 0;
	right: 0;
	z-index: 99;
	border: 1px solid #37434f;
	border-top: none;
	border-radius: 0 0 7px 7px;
}
.select-hide {
	display: none;
}
.select-items div:hover, 
.same-as-selected {
	background-color: rgba(0, 0, 0, 0.1);
}

// #vue-trading-view{
// 	position: relative;
// 	// padding-bottom: 62.24%;
// 	// padding-bottom: 93.5%;
// 	padding-bottom: 50%;
// 	// min-height: 730px;
// 	// padding-bottom: 100%;
// 	@include max-screen(1280px) {
// 		min-height: auto;
// 	}
// 	iframe{
// 		position: absolute;
// 		top: 0;
// 		bottom: 0;
// 		left: 0;
// 		right: 0;
// 		width: 100%;
// 		height: 100%;
// 	}
// }




</style>
