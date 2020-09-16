<template>
	<div class="header">
		<div class="header_nav">
			<div class="container">
				<ul class="navs">
					<li v-for="headerNav of headerNavigation" v-bind:key="headerNav.id" class="item">
						<a href="#">{{ headerNav.name }}</a>
					</li>
				</ul>
			</div>
		</div>
		<div class="header_panel">
			<div class="container">
				<div class="cols">
					<div class="col first">
						<button type="button" class="hamburger">
							<span></span>
						</button>
					</div>
					<div class="col">
						<div class="logo">
							<a href="#">
								<svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30">
									<defs>
									<linearGradient id="93bsa" x1="0" x2="30" y1="0" y2="30"
										gradientUnits="userSpaceOnUse">
										<stop offset="0" stop-color="#fff" />
										<stop offset="1" stop-color="#fff" />
									</linearGradient>
									</defs>
									<g>
									<g opacity=".9">
										<path fill="url(#93bsa)"
										d="M28.03 22.457c.1-.237.203-.406.304-.542 1.152-2.267 1.728-4.67 1.66-7.207-.169-4.365-1.897-7.985-5.116-10.895-.237-.237-.407-.169-.61 0-1.288.981-2.575 1.929-3.863 2.91-.068.068-.17.135-.271.237.136.068.237.169.339.237a10.034 10.034 0 0 1 3.083 3.552c.136.237.068.406-.101.576-.644.643-1.254 1.285-1.898 1.928-.237.237-.237.406-.034.677 1.525 1.962 3.016 3.959 4.507 5.921.644.846 1.288 1.692 2 2.606zM22.515 2.155c-.034-.034-.034-.067-.034-.169-.102-.068-.203-.101-.305-.17C19.465.363 16.549-.246 13.497.092 9.634.497 6.413 2.19 3.802 5.065c-.237.237-.203.406-.033.643.508.677 1.017 1.387 1.56 2.098.508.676 1.016 1.32 1.559 2.03.067-.102.135-.203.203-.27.95-1.32 2.102-2.37 3.56-3.114.237-.101.407-.067.576.102.61.643 1.255 1.218 1.865 1.86.203.238.373.204.61.035 1.831-1.32 3.696-2.673 5.56-3.993 1.085-.744 2.17-1.523 3.255-2.3zM9.866 23.167c-.202-.135-.338-.237-.507-.338-1.22-.914-2.203-2.03-2.915-3.384-.135-.237-.101-.406.102-.609a60.386 60.386 0 0 0 2.067-2.098c.068-.067.102-.135.17-.236-2.237-2.944-4.507-5.888-6.744-8.832-.067.034-.101.034-.101.068-.034.068-.102.17-.136.237C.176 11.054-.366 14.302.243 17.72c.61 3.383 2.237 6.225 4.812 8.526.271.237.44.237.678.034.576-.44 1.152-.846 1.728-1.286.78-.609 1.559-1.184 2.406-1.827zm13.318-2.977c-.102.067-.136.067-.102.067-.034.068-.102.136-.135.203a9.392 9.392 0 0 1-3.118 2.876c-.915.508-.644.474-1.355-.203-.644-.609-1.288-1.252-1.966-1.894-3.015 2.233-5.997 4.466-9.047 6.733 3.422 1.895 6.946 2.47 10.674 1.692 3.354-.711 6.133-2.403 8.37-5.042-1.119-1.489-2.237-2.977-3.321-4.432z" />
									</g>
									</g>
								</svg>
								<span>Crypto<em>Dash</em></span>
							</a>
						</div>
					</div>
					<div class="col second">
						<div class="wrap_container">
							<div class="list">
								<div class="item" v-for="val of valItem" v-bind:key="val.id">
									<img :src="'./img/' + val.icon + '.svg'" :alt="val.icon">
									<div class="label">
										<div class="name">{{ val.name }} {{ val.cur }} $<strong>{{ val.num }}</strong></div>
										<div class="count" :class="val.directing">
											<div class="icon">
												<i class="icon-arrow-up"></i>
											</div>
											<span>{{ val.percent }}%</span>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
					<div class="col last">
						<div class="columns_balance">
							<div v-for="headerColumnBalance of headerColumnsBalance" v-bind:key="headerColumnBalance.id" class="column">
								<em>{{ headerColumnBalance.num }}</em> <span><i>{{ headerColumnBalance.name }}</i> <strong>{{ headerColumnBalance.second }}</strong></span>
							</div>
						</div>
						<div class="wrap_lang">
							<div class="view_lang">
								<div class="wrap_flag">
									<img src="../images/flags/ru.svg" alt="">
								</div>
								<span>EN</span>
								<i class="icon-arrow-drop-down"></i>
							</div>
							<div class="drop_lang">
								<a href="#" class="item_lang" v-for="lang of langItem" v-bind:key="lang.id">
									<img :src="'img/' + lang.icon + '.svg'" alt="">
									<span>{{ lang.name }}</span>
								</a>
							</div>
						</div>
						<div class="wrap_reminder">
							<div class="view_reminder">
								<i class="icon-bell"></i>
								<!-- <span v-bind="notify.id">{{notify.num}}</span> -->
								<span>45</span>
							</div>
						</div>
						<div class="login_panel">
							<div class="view_user">
								<div class="wrap">
									Вы вошли как
									<div class="name_user">Razersection</div>
								</div>
								<div class="avatar">
									<img src="../images/avatar.jpg" alt="">
								</div>
								<i class="icon-arrow-drop-down"></i>
							</div>
							<div class="drop_user">
								<div class="drop_information">
									<div class="top">
										<div class="avatar">
											<img src="../images/avatar.jpg" alt="">
										</div>
										<div class="user_info">
											<a href="#" class="name"><strong>Razersection</strong></a>
											<a href="mailto:alex@gmail.com"><strong>alex@gmail.com</strong></a>
										</div>
										<button type="button" class="close">
											<i class="icon-close"></i>
										</button>
									</div>
									<ul class="bottom_list">
										<li>Last login: <span>24 Apr 2020</span></li>
										<li>Any system info</li>
									</ul>
								</div>
								<div class="drop_nav">
									<a href="#" class="nav_item">
										<i class="icon-settings"></i>
										<span>Личные Данные</span>
									</a>
									<a href="#" class="nav_item">
										<i class="icon-papper"></i>
										<span>Статьи</span>
									</a>
									<a href="#" class="nav_item">
										<i class="icon-chat-fill"></i>
										<span>Чат</span>
									</a>
									<a href="#" class="nav_item">
										<i class="icon-statistic"></i>
										<span>Опция меню 4</span>
									</a>
									<a href="#" class="nav_item">
										<i class="icon-menu"></i>
										<span>Опция меню 5</span>
									</a>
									<a href="#" class="nav_item second">
										<i class="icon-logout"></i>
										<span>Выход</span>
									</a>
								</div>
							</div>
						</div>
						<div class="second_block">
							<button type="button" class="btn">
								<i class="icon-logout"></i>
							</button>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="header_bottom">
			<div class="container">
				<div class="wrap_container">
					<div class="cols">
						<div v-for="headerNavInfo of headerNavigationInformation" v-bind:key="headerNavInfo.id" class="item">
							<div class="icon">
								<i :class="headerNavInfo.icon"></i>
							</div>
							<div class="wrap">
								<strong>{{ headerNavInfo.num }}</strong>
								<span>{{ headerNavInfo.name }}</span>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="mobile_menu">
			<div class="wrap_lang">
				<div class="view_lang">
					<div class="wrap_flag">
						<img src="../images/flags/ru.svg" alt="">
					</div>
					<span>EN</span>
					<i class="icon-arrow-drop-down"></i>
				</div>
				<div class="drop_lang">
					<a href="#" class="item_lang" v-for="lang of langItem" v-bind:key="lang.id">
						<img :src="'img/' + lang.icon + '.svg'" alt="">
						<span>{{ lang.name }}</span>
					</a>
				</div>
			</div>
			<div class="nav">
				<div v-for="headerNav of headerNavigation" v-bind:key="headerNav.id" class="item">
					<a href="#">{{ headerNav.name }}</a>
				</div>
			</div>
			<div class="nav_footer">
				<ul class="list_social">
					<li v-for="footerNavSocial of footerNavigationSocial" v-bind:key="footerNavSocial.id" class="item_social">
						<a href="#">
							<i :class="footerNavSocial.icon"></i>
						</a>
					</li>
				</ul>
				<ul class="list">
					<li class="list_item"><a href="#">Privacy Policy</a></li>
					<li class="list_item"><a href="#">Terms of use</a></li>
				</ul>
				<div class="column">Copyright &copy; {{ new Date().getFullYear() }} Crytodash</div>
			</div>
		</div>
	</div>
</template>

<script>
	import Vue from 'vue'

	var blogURL = 'https://html-cafe.com/out/crypto-portal/contentJSON.json'

	export default {
		data: function () {
			return {
				headerNavigation: headerNavItems,
				headerColumnsBalance: headerInfoBalance,
				valItem: headerValItem,
				headerNavigationInformation: headerNavInfoItems,
				langItem: headerLangItems,
				footerNavigationSocial: footerNavSocialItems
			}
		},
		created: function(){
			this.fetchData();
		},
		methods:{
			fetchData: function(){
				var xhr = new XMLHttpRequest();
				xhr.open('GET', blogURL);
				xhr.onload = function(){
					const contentObj = JSON.parse(xhr.responseText);
					contentObj.headerListNavigation.forEach(e => {
						headerNavItems.push(headerNavigationCore(e.name));
					});
					contentObj.headerListBalance.forEach(e => {
						// console.log(e);
						headerInfoBalance.push(headerBalanceCore(e.name, e.num, e.second));
					});
					contentObj.headerValCurrList.forEach(e => {
						headerValItem.push(headerValCore(e.directing, e.icon, e.name, e.cur, e.num, e.percent));
					});
					contentObj.headerListInfo.forEach(e => {
						headerNavInfoItems.push(headerInformationCore(e.name, e.num, e.icon));
					});
					contentObj.langDrop.forEach(e => {
						headerLangItems.push(headerLangCore(e.name, e.icon));
					});
					contentObj.footerListSocial.forEach(e => {
						footerNavSocialItems.push(footerNavigationSocialCore(e.icon));
					});
					// console.log(listInfoBalance);
				}
				xhr.send();
			}
		},
		mounted() {
			langDrop();
			userPanel();
			mobileMenu();
		}
	}

	//functions core
	function headerNavigationCore(name) {
	
		// console.log(name, num, icon, second);
		// var args = Array.from(arguments).toString();
		// var args = Array.from(arguments).join();

		// console.log(args);
		
		// return args
		
		return {
			name
		}
	}
	function headerBalanceCore(name, num, second) {
		return {
			name,
			num,
			second
		}
	}
	function headerValCore(directing, icon, name, cur, num, percent) {
		return {
			directing,
			icon,
			name,
			cur,
			num,
			percent
		}
	}
	function headerInformationCore(name, num, icon) {
		return {
			name,
			num,
			icon
		}
	}
	function headerLangCore(name, icon) {
		return {
			name,
			icon
		}
	}
	function footerNavigationSocialCore(icon) {
		return {
			icon
		}
	}

	const headerNavItems = [];
	const headerInfoBalance = [];
	const headerValItem = [];
	const headerNavInfoItems = [];
	const headerLangItems = [];
	const footerNavSocialItems = [];

	new Vue({
		data: {
			headerNavigation: headerNavItems,
			headerColumnsBalance: headerInfoBalance,
			valItem: headerValItem,
			headerNavigationInformation: headerNavInfoItems,
			langItem: headerLangItems,
			footerNavigationSocial: footerNavSocialItems
		}
	});

	//functions --
	//lang Droppped
	function langDrop() {
		var specifiedElement = document.querySelectorAll('.wrap_lang');
		document.addEventListener('click', function (event) {
			for (var i = 0; i < specifiedElement.length; i++) {
				var isClickInside = specifiedElement[i].contains(event.target);
				if (isClickInside) {
					specifiedElement[i].classList.toggle('open');
				} else {
					specifiedElement[i].classList.remove('open');
				}
			}
		});
	}

	//User Panel
	function userPanel() {
		let openBtn = document.querySelector('.view_user'),
			closeBtn = document.querySelector('.close'),
			wrapper = document.querySelector('.login_panel');

		openBtn.addEventListener('click', toggleDrop);
		closeBtn.addEventListener('click', toggleDrop);
		document.addEventListener('click', removeClass);
		
		function toggleDrop() {
			wrapper.classList.toggle('open');
		}

		function removeClass() {
			var isClickInside = wrapper.contains(event.target);

			if (!isClickInside) {
				wrapper.classList.remove('open');
			}
		}
	}

	//Mobile Menu
	function mobileMenu() {
		let openBtn = document.querySelector('.hamburger'),
			wrapper = document.querySelector('.header'),
			menu = document.querySelector('.mobile_menu');
		
		openBtn.addEventListener('click', toggleDrop);
		document.addEventListener('click', removeClass);

		function toggleDrop() {
			wrapper.classList.toggle('open');
			document.body.classList.toggle('open');
		}
		function removeClass(e) {
			if (wrapper.classList.contains('open') && !openBtn.contains(e.target)) {
				var isClickInside = menu.contains(e.target);
				
				if (!isClickInside) {
					wrapper.classList.remove('open');
					document.body.classList.remove('open');
				}
			}
		}
	}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

.header{
	position: relative;
	z-index: 999;
	@include max-screen(1160px) {
		&.open{
			.hamburger{
				span,
				&:before,
				&:after{
					width: 28px;
				}
			}
			.mobile_menu{
				transform: translate3d(0, 0, 0) rotateY(0);
				opacity: 1;
				visibility: visible;
			}
		}
	}
}
.header_nav{
	background-color: #253443;
	margin-bottom: 5px;
	@include max-screen(1160px) {
		display: none;
	}
}
.navs{
	display: flex;
	justify-content: space-between;
	margin: 0 -10px;
	.item{
		font-size: 15px;
		padding: 0 10px;
		text-align: center;
		&.active{
			a{
				color: #008aff;
				&:after{
					transform: translate3d(0, 0, 0);
				}
			}
		}
	}
	a{
		color: #fff;
		transition: color .3s;
		display: flex;
		align-items: center;
		padding: 15px 0;
		height: 100%;
		position: relative;
		overflow: hidden;
		@include min-screen(1025px) {
			&:hover{
				color: #008aff;
				&:after{
					transform: translate3d(0, 0, 0);
				}
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
			transform: translate3d(0, 2px, 0);
			transition: transform .3s;
		}
	}
}
.header_panel{
	background-color: #253443;
	padding: 10px 0;
	.cols{
		display: flex;
		align-items: center;
		margin: 0 -10px;
		@include max-screen(1160px) {
			flex-wrap: wrap;
		}
	}
	.col{
		padding: 0 10px;
		flex-shrink: 0;
		flex-grow: 0;
		display: flex;
		&.first{
			display: none;
			@include max-screen(1160px) {
				display: block;
			}
		}
		&.second{
			margin: 0;
			flex-shrink: 1;
			flex-grow: 1;
			min-width: 1px;
			display: flex;
			justify-content: flex-end;
			@include max-screen(1160px) {
				order: 3;
				padding: 0;
				margin: 10px -20px -10px;
				background-color: #19232c;
			}
		}
		&.last{
			@include max-screen(1160px) {
				flex-shrink: 1;
				flex-grow: 1;
				min-width: 1px;
				justify-content: flex-end;
			}
		}
	}
	.wrap_container{
		@include max-screen(1160px) {
			overflow: hidden;
			width: 100%;
			white-space: nowrap;
			display: flex;
			overflow: hidden;
			white-space: nowrap;
			position: relative;
			&:after{
				content: "";
				position: absolute;
				top: 0;
				bottom: 0;
				right: 0;
				width: 40px;
				background: linear-gradient(to right,  rgba(35,45,56,0) 0%,rgba(35,45,56,0.5) 50%,rgba(35,45,56,1) 100%);
				filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00232d38', endColorstr='#232d38',GradientType=1 );
			}
		}
	}
	.list{
		display: flex;
		align-items: center;
		margin: 0 -10px;
		@include max-screen(1160px) {
			flex-shrink: 1;
			flex-grow: 1;
			min-width: 1px;
			padding: 25px 30px;
			overflow-x: scroll;
		}
	}
	.item{
		display: flex;
		align-items: center;
		padding: 0 10px;
		svg,
		img{
			flex-shrink: 0;
			flex-grow: 0;
			margin-right: 10px;
		}
	}
	.label{
		display: flex;
		flex-wrap: wrap;
		align-items: center;
	}
	.name{
		margin-right: 8px;
	}
	.count{
		display: flex;
		align-items: center;
		color: #ccc;
		&.up{
			color: #56e39e;
		}
		&.down{
			color: #ff5353;
			i{
				transform: rotate(180deg);
			}
		}
	}
	.icon{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 8px;
		i{
			font-size: 9px;
			display: block;
		}
	}
	.wrap_lang{
		margin-left: 20px;
		@include max-screen(767px) {
			display: none;
		}
	}
}

/* //hamburger */
.hamburger{
	position: relative;
	width: 28px;
	height: 20px;
	background: none;
	border: none;
	cursor: pointer;
	&:before,
	&:after{
		content: "";
		position: absolute;
		left: 0;
		height: 2px;
		background-color: #fff;
		border-radius: 4px;
		transition: width .3s;
	}
	&:before{
		top: 0;
		width: 28px;
	}
	&:after{
		width: 16px;
		bottom: 0;
	}
	span{
		position: absolute;
		top: 50%;
		left: 0;
		transform: translate3d(0, -50%, 0);
		width: 22px;
		height: 2px;
		background-color: #fff;
		border-radius: 4px;
		transition: width .3s;
	}
}

/* //logo */
.logo{
	display: flex;
	font-size: 15px;
	a{
		display: flex;
		align-items: center;
		color: #fff;
	}
	svg{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 8px;
	}
	span{
		font-weight: 300;
	}
	em{
		font-style: normal;
		font-weight: 900;
	}
}

/* //balance */
.columns_balance{
	display: flex;
	background-color: #202933;
	padding: 5px 0;
	@include max-screen(600px) {
		display: none;
	}
	.column{
		padding: 5px 15px;
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
		position: relative;
		font-size: 18px;
		line-height: 1;
		display: flex;
		align-items: flex-end;
		@include max-screen(1440px) {
			flex-direction: column;
		}
		@include max-screen(1160px) {
			flex-direction: row;
		}
		&:first-child{
			&:after{
				display: none;
			}
		}
		&:after{
			content: "";
			position: absolute;
			top: 0;
			left: 0;
			bottom: 0;
			height: 100%;
			width: 1px;
			background-color: #303c5d;
		}
	}
	em{
		line-height: .9;
	}
	span{
		color: #bac9dd;
		font-size: 12px;
		padding-left: 5px;
	}
	i{
		font-style: normal;
		@include max-screen(1366px) {
			display: none;
		}
	}
	strong{
		@include max-screen(1366px) {
			display: block;
		}
	}
}

/* //lang */
.wrap_lang{
	display: flex;
	align-items: center;
  color: #fff;
	cursor: pointer;
	border-radius: 8px;
	position: relative;
	z-index: 2;
	background-color: #1c222b;
	&.open{
		border-radius: 8px 8px 0 0;
		.view_lang{
			i{
				transform: rotate(180deg);
			}
		}
		.drop_lang{
			transform: translate3d(0, 0, 0);
			opacity: 1;
			visibility: visible;
		}
	}
}
.drop_lang{
	position: absolute;
	top: 100%;
	left: 0;
	right: 0;
	background-color: #1c222b;
	border-radius: 0 0 8px 8px;
	transform: translate3d(0, 10px, 0);
	opacity: 0;
	visibility: hidden;
	transition: transform .3s, opacity .3s, visibility .3s;
}
.item_lang{
	display: flex;
	padding: 10px 20px;
	border: 1px solid transparent;
	color: #fff;
	@include min-screen(1025px) {
		&:hover{
			border: 1px solid #37434f;
			background-color: #2e3842;
			&:last-child{
				border-radius: 0 0 8px 8px;
			}
		}
	}
	img{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 10px;
	}
	span{
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
	}
}
.wrap_flag{
	margin-right: 10px;
	img{
		display: inline-block;
		vertical-align: top;
		max-width: 100%;
		height: auto;
	}
}
.view_lang{
	display: flex;
	height: 100%;
	padding: 0 20px;
	align-items: center;
	span{
		margin-right: 14px;
	}
	i{
		color: #788797;
		font-size: 10px;
	}
}

/* //reminder */
.wrap_reminder{
	display: flex;
	align-items: center;
	margin-left: 20px;
	@include max-screen(479px) {
		margin: 0;
	}
}
.view_reminder{
	color: #fff;
	position: relative;
	i{
		font-size: 20px;
	}
	span{
		position: absolute;
		top: -8px;
		right: -8px;
		width: 18px;
		height: 18px;
		font-size: 11px;
		font-weight: 500;
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 9px;
		background-color: #f62650;
	}
}

/* //panel profile */
.login_panel{
	position: relative;
	z-index: 2;
	display: flex;
	margin-left: 40px;
	@include max-screen(479px) {
		margin-left: 20px;
	}
	&.open{
		.drop_user{
			transform: translate3d(0, 0, 0);
			opacity: 1;
			visibility: visible;
		}
	}
}
.view_user{
	display: flex;
	align-items: center;
	cursor: pointer;
	color: #788797;
	.wrap{
		text-align: right;
		color: #8999a9;
		font-size: 13px;
		line-height: 1.25;
		margin-right: 15px;
		@include max-screen(1366px) {
			display: none;
		}
	}
	.name_user{
		color: #fff;
	}
	.avatar{
		width: 36px;
		height: 36px;
		border-radius: 10px;
		overflow: hidden;
		img{
			display: block;
			width: 100%;
			height: auto;
		}
	}
	i{
		font-size: 10px;
		margin-left: 10px;
	}
}

/* //drop */
.drop_user{
	position: absolute;
	width: 280px;
	top: -10px;
	right: 0;
	border-radius: 8px;
	overflow: hidden;
	background-color: #232d38;
	transform: translate3d(100%, 0, 0);
	opacity: 0;
	visibility: hidden;
	transition: transform .3s, opacity .3s, visibility .3s;
}
.drop_information{
	padding: 20px;
	background-color: #37434f;
	position: relative;
	.top{
		display: flex;
	}
	.avatar{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 20px;
		width: 36px;
		height: 36px;
		border-radius: 10px;
		overflow: hidden;
		img{
			display: block;
			width: 100%;
			height: auto;
		}
	}
	.user_info{
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		font-size: 16px;
		line-height: 1.2;
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
		strong{
			display: inline-block;
			vertical-align: top;
			white-space: nowrap;
			max-width: 100%;
			overflow: hidden;
			text-overflow: ellipsis;
		}
	}
	a{
		color: #008aff;
		max-width: 100%;
		@include min-screen(1025px) {
			&:hover{
				text-decoration: underline;
			}
		}
	}
	.name{
		color: #fff;
		margin: 0;
	}
	.close{
		position: absolute;
		top: 0;
		right: 0;
		background: none;
		border: none;
		cursor: pointer;
		color: #abb6c2;
		padding: 14px;
		transition: color .3s;
		@include min-screen(1025px) {
			&:hover{
				color: #fff;
			}
		}
		i{
			font-size: 12px;
		}
	}
}
.bottom_list{
	margin-top: 8px;
	color: #abb6c2;
	font-size: 12px;
	font-weight: 300;
	line-height: 1;
	display: flex;
	li{
		border-left: 1px solid #fff;
		padding-left: 10px;
		margin-left: 10px;
		&:first-child{
			border-left: none;
			margin-left: 0;
			padding-left: 0;
		}
	}
	span{
		color: #fff;
	}
}
.drop_nav{
	border: 1px solid #37434f;
	border-radius: 0 0 8px 8px;
}
.nav_item{
	color: #788797;
	font-size: 14px;
	font-weight: 500;
	line-height: 1.2;
	display: flex;
	align-items: center;
	padding: 14px 20px;
	position: relative;
	&:last-child{
		border-bottom: none;
	}
	&.second{
		border-top: 1px solid #37434f;
	}
	&:after{
		content: "";
		position: absolute;
		top: 50%;
		right: 15px;
		transform: translate3d(0, -50%, 0);
		width: 0;
		height: 0;
		border-top: 5px solid transparent;
		border-left: 5px solid #008aff;
		border-bottom: 5px solid transparent;
		transform: translate3d(-10px, 0, 0);
		opacity: 0;
		visibility: hidden;
		transition: transform .3s, opacity .3s, visibility .3s;
	}
	@include min-screen(1025px) {
		&:hover{
			background-color: #2e3842;
			box-shadow: 0 0 0 1px #37434f;
			&:after{
				transform: translate3d(0, 0, 0);
				opacity: 1;
				visibility: visible;
			}
			i{
				color: #008aff;
			}
			&.second{
				box-shadow: none;
			}
		}
	}
	span{
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
		padding: 0 10px 0 0;
	}
	i{
		font-size: 16px;
		flex-shrink: 0;
		width: 16px;
		display: flex;
		justify-content: center;
		flex-grow: 0;
		margin-right: 20px;
	}
}

//
.second_block{
	display: flex;
	align-items: center;
	border-left: 1px solid #37434f;
	padding-left: 22px;
	margin-left: 22px;
	@include max-screen(860px) {
		display: none;
	}
	.btn{
		background: none;
		border: none;
		cursor: pointer;
		color: #788797;
		padding: 0;
		transition: color .3s;
		@include min-screen(1025px) {
			&:hover{
				color: #008aff;
			}
		}
		i{
			font-size: 20px;
		}
	}
}

/* //header bottom */
.header_bottom{
	box-shadow: 0 2px 6px rgba(0, 0, 0, 0.11);
	background-image: linear-gradient(to right, #232d38 0%, #253443 52%, #232d38 100%);
	border-top: 1px solid #37434f;
	.wrap_container{
		overflow: hidden;
		width: 100%;
		white-space: nowrap;
		display: flex;
		position: relative;
		&:after{
			content: "";
			position: absolute;
			top: 0;
			bottom: 0;
			right: 0;
			width: 40px;
			background: linear-gradient(to right,  rgba(35,45,56,0) 0%,rgba(35,45,56,0.5) 50%,rgba(35,45,56,1) 100%);
			filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00232d38', endColorstr='#232d38',GradientType=1 );
		}
	}
	.container{
		padding: 0;
	}
	.cols{
		display: flex;
		flex-shrink: 1;
		flex-grow: 1;
		min-width: 1px;
		overflow-x: auto;
		padding: 25px 20px;
	}
	.item{
		padding: 0 20px;
		display: flex;
		align-items: center;
		flex-shrink: 1;
		flex-grow: 1;
    min-width: 1px;
		justify-content: center;
		border-left: 1px solid #37434f;
		@include max-screen(1460px) {
			flex-shrink: 0;
			flex-grow: 0;
		}
		&:first-child{
			justify-content: flex-start;
			border-left: none;
			padding-left: 0;
		}
		&:last-child{
			justify-content: flex-end;
		}
	}
	.icon{
		flex-shrink: 0;
		flex-grow: 0;
		margin-right: 15px;
		i{
			font-size: 30px;
			&.icon-hands,
			&.icon-up-statistic {
				color: #008aff;
			}
			&.icon-circle-accept,
			&.icon-target, 
			&.icon-cash {
				color: #56e39e;
			}
			&.icon-n-smile{
				color: #f62650;
			}
		}
	}
	.wrap{
		display: flex;
		align-items: center;
	}
	strong{
		margin-right: 15px;
		color: #fff;
		font-size: 32px;
		font-weight: 900;
		flex-shrink: 0;
		flex-grow: 0;
	}
	em{
		font-weight: 300;
		font-size: 32px;
	}
	span{
		color: #8999a9;
		font-size: 16px;
		flex-shrink: 0;
		flex-grow: 0;
	}
}

/* //mobile */
.mobile_menu{
	position: fixed;
	top: 56px;
	left: 0;
	bottom: 0;
	overflow: auto;
	display: flex;
	flex-direction: column;
	align-items: flex-start;
	z-index: 999;
	padding: 20px 50px 60px;
	max-width: 510px;
	transform: translate3d(-45px, 0, 0) rotateY(-90deg);
	transform-origin: 0 100%;
	transition: transform .6s, opacity .6s, visibility .6s;
	width: 100%;
	box-shadow: 0 -5px 10px rgba(0, 0, 0, 0.15);
	background-image: linear-gradient(180deg, #303b4d 0%, #202a34 100%);
	@include max-screen(480px) {
		max-width: 300px;
	}
	.wrap_lang{
		flex-shrink: 0;
		flex-grow: 0;
		margin-bottom: 30px;
	}
	.view_lang{
		padding: 10px 20px;
	}
	.nav{
		flex-shrink: 1;
		flex-grow: 1;
		min-height: 1px;
		overflow: auto;
		min-height: 125px;
		margin-bottom: 20px;
	}
	.item{
		font-size: 15px;
		margin-bottom: 30px;
		&:last-child{
			margin-bottom: 0;
		}
	}
	a{
		color: #fff;
	}
}
.nav_footer{
	flex-shrink: 0;
	flex-grow: 0;
	color: #9299a1;
	.list_social{
		margin-bottom: 30px;
	}
	.list{
		display: flex;
		margin: -6px;
		padding-bottom: 25px;
		a{
			color: #bfcefb;
		}
	}
	.list_item{
		padding: 6px;
		position: relative;
		&:first-child{
			&:before{
				display: none;
			}
		}
		&:before{
			content: "";
			position: absolute;
			top: 50%;
			transform: translate3d(0, -50%, 0);
			left: 0;
			width: 1px;
			height: 10px;
			background-color: #bfcefb;
		}
	}
}
.list_social{
	display: flex;
	flex-wrap: wrap;
	margin: -4px;
}
.item_social{
	padding: 4px;
	a{
		background-color: #e6f0ff;
		display: flex;
		align-items: center;
		justify-content: center;
		border-radius: 30px;
		width: 30px;
		height: 30px;
		color: #008aff;
		opacity: .8;
		transition: opacity .3s;
		@include min-screen(1025px) {
			&:hover{
				text-decoration: none;
				opacity: 1;
			}
		}
	}
	i{
		font-size: 17px;
	}
}
</style>
