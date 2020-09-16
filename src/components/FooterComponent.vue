<template>
	<div class="footer">
		<div class="container">
			<div class="cols">
				<div class="col">
					<div class="logo_footer">
						<a href="#">
							<svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30">
								<defs>
									<linearGradient id="93bsa" x1="0" x2="30" y1="0" y2="30" gradientUnits="userSpaceOnUse">
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
					<div class="list_column">
						<div class="column">
							<ul class="list_social">
								<li v-for="footerNavSocial of footerNavigationSocial" v-bind:key="footerNavSocial.id" class="item_social">
									<a href="#">
										<i :class="footerNavSocial.icon"></i>
									</a>
								</li>
							</ul>
						</div>
						<div class="column">Copyright &copy; {{ new Date().getFullYear() }} Crytodash</div>
					</div>
				</div>
				<div class="col latest">
					<ul class="list">
						<li v-for="footerNavTerms of footerNavigationTerms" v-bind:key="footerNavTerms.id" class="item">
							<a href="#">{{ footerNavTerms.name }}</a>
						</li>
					</ul>
				</div>
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
				footerNavigationTerms: footerNavTermsItems,
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
					// console.log(contentObj);
					contentObj.footerListSocial.forEach(e => {
						footerNavSocialItems.push(footerNavigationSocialCore(e.icon));
					});
					contentObj.footerListTerms.forEach(e => {
						footerNavTermsItems.push(footerNavigationTermsCore(e.name));
					});
				}
				xhr.send();
			}
		}
	}

	//functions core
	function footerNavigationTermsCore(name) {
		return {
			name
		}
	}
	function footerNavigationSocialCore(icon) {
		return {
			icon
		}
	}

	const footerNavTermsItems = [];
	const footerNavSocialItems = [];

	new Vue({
		data: {
			footerNavigationTerms: footerNavTermsItems,
			footerNavigationSocial: footerNavSocialItems
		}
	});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

//footer
.footer{
	display: table-row;
	height: 1px;
	background-color: #253443;
	@include max-screen(640px) {
		display: none;
	}
	.cols{
		padding: 22px 0;
		display: flex;
		align-items: center;
		@include max-screen(860px) {
			flex-direction: column;
		}
	}
	.col{
		flex-grow: 0;
		flex-shrink: 0;
		max-width: 330px;
		width: 100%;
		@include max-screen(1440px) {
			max-width: 100%;
			width: auto;
			padding-right: 24px;
		}
		@include max-screen(860px) {
			padding: 0;
			margin-bottom: 20px;
			&:last-child{
				margin-bottom: 0;
			}
		}
		&.second{
			flex-shrink: 1;
			flex-grow: 1;
			min-width: 1px;
			max-width: 100%;
			border-left: 1px solid #37434f;
			@include max-screen(860px) {
				border: none;
			}
		}
		&.latest{
			max-width: 100%;
			width: auto;
		}
	}
	.list{
		display: flex;
		margin: 0 -8px;
	}
	.item{
		font-size: 14px;
		line-height: 1.2;
		padding: 0 8px;
		border-left: 1px solid #bfcefb;
		&:first-child{
			border: none;
		}
	}
	a{
		color: #bfcefb;
		@include min-screen(1025px) {
			&:hover{
				text-decoration: underline;
			}
		}
	}
}

//logo
.logo_footer{
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

//list nav
.list_column{
	display: flex;
	padding-left: 24px;
	.column{
		padding-left: 22px;
		margin-left: 22px;
		display: flex;
		align-items: center;
		border-left: 1px solid #37434f;
		color: #9299a1;
		&:first-child{
			margin-left: 0;
			padding-left: 0;
			border: none;
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
