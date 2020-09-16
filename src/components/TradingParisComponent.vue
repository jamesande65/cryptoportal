<template>
	<div class="aside">
		<div class="box_aside" id="exchanges">
			<form action="#" class="aside_accordion">
				<div class="heading">
					<h2 class="title">Торговые пары</h2>
				</div>
				<div class="sub_heading">
					<div class="col">
						<div class="custom-select">
							<select>
								<option value="0">Выбрать:</option>
								<option value="1">XYZ Exchange 1</option>
								<option value="2">XYZ Exchange 2</option>
							</select>
						</div>
					</div>
					<div class="col second">
						<div class="wrap_input">
							<input type="text" class="input" value="LTC">
							<button type="submit" class="btn_search">GO</button>
						</div>
					</div>
				</div>
				<div class="accordion_heading">
					<table>
						<tr>
							<th>Биржа/Пара</th>
							<th>Цена</th>
							<th>Change</th>
						</tr>
					</table>
				</div>
				<div class="accordion_content">
					<div class="scrollscreen">
						<div v-for="tradingAccordionNav of tradingAccordionNavigation" v-bind:key="tradingAccordionNav.id" class="item">
							<button type="button" class="button" v-on:click="showHideSector">
								<strong>{{ tradingAccordionNav.name }}</strong>
								<em>({{ tradingAccordionNav.num }})</em>
								<i class="icon-arrow-drop-down"></i>
							</button>
							<div class="hidden">
								<table>
									<tr>
										<td>
											<div class="name">
												<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 30 30">
													<g>
														<g clip-path="url(#clip-005E2401-079E-1234-50F1-94958D2086FA)" opacity=".9">
															<path fill="#f7931a"
																d="M29.548 18.629c-2.003 8.036-10.142 12.926-18.18 10.922C3.336 27.547-1.554 19.408.45 11.373 2.452 3.336 10.591-1.555 18.625.45c8.036 2.003 12.926 10.144 10.923 18.18">
															</path>
														</g>
														<g opacity=".9">
															<path fill="#fff"
																d="M19.357 15.558c1.504.778 2.269 1.971 1.54 4.04-.905 2.57-3.054 2.787-5.912 2.25l-.694 2.763-1.676-.415.685-2.727a63.298 63.298 0 0 1-1.336-.344l-.687 2.74-1.674-.416.694-2.769c-.392-.1-.79-.206-1.195-.307l-2.182-.54.833-1.907s1.234.326 1.217.302c.475.117.685-.191.769-.396l1.096-4.368.177.043a1.373 1.373 0 0 0-.174-.055l.782-3.118c.02-.355-.103-.801-.782-.97.027-.017-1.216-.3-1.216-.3l.445-1.78 2.312.574-.002.008c.348.086.706.168 1.07.25l.687-2.736 1.675.415-.673 2.683c.45.102.903.205 1.343.314l.668-2.665 1.677.415-.687 2.737c2.116.725 3.664 1.811 3.36 3.832zm-5.928-.106l-.92 3.668c1.136.28 4.64 1.399 5.159-.67zm1.256-5.006l-.835 3.318c.946.234 3.863 1.187 4.336-.69z">
															</path>
														</g>
													</g>
												</svg>
												<strong>Ada</strong>
											</div>
										</td>
										<td>1436.99</td>
										<td>
											<div class="rate negative">
												<i class="icon-arrow-up"></i>
												<span>6.84%</span>
											</div>
										</td>
									</tr>
									<tr>
										<td>
											<div class="name">
												<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 30 30">
													<g>
														<g clip-path="url(#clip-005E2401-079E-1234-50F1-94958D2086FA)" opacity=".9">
															<path fill="#f7931a"
																d="M29.548 18.629c-2.003 8.036-10.142 12.926-18.18 10.922C3.336 27.547-1.554 19.408.45 11.373 2.452 3.336 10.591-1.555 18.625.45c8.036 2.003 12.926 10.144 10.923 18.18">
															</path>
														</g>
														<g opacity=".9">
															<path fill="#fff"
																d="M19.357 15.558c1.504.778 2.269 1.971 1.54 4.04-.905 2.57-3.054 2.787-5.912 2.25l-.694 2.763-1.676-.415.685-2.727a63.298 63.298 0 0 1-1.336-.344l-.687 2.74-1.674-.416.694-2.769c-.392-.1-.79-.206-1.195-.307l-2.182-.54.833-1.907s1.234.326 1.217.302c.475.117.685-.191.769-.396l1.096-4.368.177.043a1.373 1.373 0 0 0-.174-.055l.782-3.118c.02-.355-.103-.801-.782-.97.027-.017-1.216-.3-1.216-.3l.445-1.78 2.312.574-.002.008c.348.086.706.168 1.07.25l.687-2.736 1.675.415-.673 2.683c.45.102.903.205 1.343.314l.668-2.665 1.677.415-.687 2.737c2.116.725 3.664 1.811 3.36 3.832zm-5.928-.106l-.92 3.668c1.136.28 4.64 1.399 5.159-.67zm1.256-5.006l-.835 3.318c.946.234 3.863 1.187 4.336-.69z">
															</path>
														</g>
													</g>
												</svg>
												<strong>Ada</strong>
											</div>
										</td>
										<td>336.99</td>
										<td>
											<div class="rate positive">
												<i class="icon-arrow-up"></i>
												<span>6.84%</span>
											</div>
										</td>
									</tr>
									<tr>
										<td>
											<div class="name">
												<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 30 30">
													<g>
														<g clip-path="url(#clip-005E2401-079E-1234-50F1-94958D2086FA)" opacity=".9">
															<path fill="#f7931a"
																d="M29.548 18.629c-2.003 8.036-10.142 12.926-18.18 10.922C3.336 27.547-1.554 19.408.45 11.373 2.452 3.336 10.591-1.555 18.625.45c8.036 2.003 12.926 10.144 10.923 18.18">
															</path>
														</g>
														<g opacity=".9">
															<path fill="#fff"
																d="M19.357 15.558c1.504.778 2.269 1.971 1.54 4.04-.905 2.57-3.054 2.787-5.912 2.25l-.694 2.763-1.676-.415.685-2.727a63.298 63.298 0 0 1-1.336-.344l-.687 2.74-1.674-.416.694-2.769c-.392-.1-.79-.206-1.195-.307l-2.182-.54.833-1.907s1.234.326 1.217.302c.475.117.685-.191.769-.396l1.096-4.368.177.043a1.373 1.373 0 0 0-.174-.055l.782-3.118c.02-.355-.103-.801-.782-.97.027-.017-1.216-.3-1.216-.3l.445-1.78 2.312.574-.002.008c.348.086.706.168 1.07.25l.687-2.736 1.675.415-.673 2.683c.45.102.903.205 1.343.314l.668-2.665 1.677.415-.687 2.737c2.116.725 3.664 1.811 3.36 3.832zm-5.928-.106l-.92 3.668c1.136.28 4.64 1.399 5.159-.67zm1.256-5.006l-.835 3.318c.946.234 3.863 1.187 4.336-.69z">
															</path>
														</g>
													</g>
												</svg>
												<strong>Ada</strong>
											</div>
										</td>
										<td>336.99</td>
										<td>
											<div class="rate negative">
												<i class="icon-arrow-up"></i>
												<span>6.84%</span>
											</div>
										</td>
									</tr>
									<tr>
										<td>
											<div class="name">
												<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 30 30">
													<g>
														<g clip-path="url(#clip-005E2401-079E-1234-50F1-94958D2086FA)" opacity=".9">
															<path fill="#f7931a"
																d="M29.548 18.629c-2.003 8.036-10.142 12.926-18.18 10.922C3.336 27.547-1.554 19.408.45 11.373 2.452 3.336 10.591-1.555 18.625.45c8.036 2.003 12.926 10.144 10.923 18.18">
															</path>
														</g>
														<g opacity=".9">
															<path fill="#fff"
																d="M19.357 15.558c1.504.778 2.269 1.971 1.54 4.04-.905 2.57-3.054 2.787-5.912 2.25l-.694 2.763-1.676-.415.685-2.727a63.298 63.298 0 0 1-1.336-.344l-.687 2.74-1.674-.416.694-2.769c-.392-.1-.79-.206-1.195-.307l-2.182-.54.833-1.907s1.234.326 1.217.302c.475.117.685-.191.769-.396l1.096-4.368.177.043a1.373 1.373 0 0 0-.174-.055l.782-3.118c.02-.355-.103-.801-.782-.97.027-.017-1.216-.3-1.216-.3l.445-1.78 2.312.574-.002.008c.348.086.706.168 1.07.25l.687-2.736 1.675.415-.673 2.683c.45.102.903.205 1.343.314l.668-2.665 1.677.415-.687 2.737c2.116.725 3.664 1.811 3.36 3.832zm-5.928-.106l-.92 3.668c1.136.28 4.64 1.399 5.159-.67zm1.256-5.006l-.835 3.318c.946.234 3.863 1.187 4.336-.69z">
															</path>
														</g>
													</g>
												</svg>
												<strong>Ada</strong>
											</div>
										</td>
										<td>336.99</td>
										<td>
											<div class="rate positive">
												<i class="icon-arrow-up"></i>
												<span>6.84%</span>
											</div>
										</td>
									</tr>
									<tr>
										<td>
											<div class="name">
												<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 30 30">
													<g>
														<g clip-path="url(#clip-005E2401-079E-1234-50F1-94958D2086FA)" opacity=".9">
															<path fill="#f7931a"
																d="M29.548 18.629c-2.003 8.036-10.142 12.926-18.18 10.922C3.336 27.547-1.554 19.408.45 11.373 2.452 3.336 10.591-1.555 18.625.45c8.036 2.003 12.926 10.144 10.923 18.18">
															</path>
														</g>
														<g opacity=".9">
															<path fill="#fff"
																d="M19.357 15.558c1.504.778 2.269 1.971 1.54 4.04-.905 2.57-3.054 2.787-5.912 2.25l-.694 2.763-1.676-.415.685-2.727a63.298 63.298 0 0 1-1.336-.344l-.687 2.74-1.674-.416.694-2.769c-.392-.1-.79-.206-1.195-.307l-2.182-.54.833-1.907s1.234.326 1.217.302c.475.117.685-.191.769-.396l1.096-4.368.177.043a1.373 1.373 0 0 0-.174-.055l.782-3.118c.02-.355-.103-.801-.782-.97.027-.017-1.216-.3-1.216-.3l.445-1.78 2.312.574-.002.008c.348.086.706.168 1.07.25l.687-2.736 1.675.415-.673 2.683c.45.102.903.205 1.343.314l.668-2.665 1.677.415-.687 2.737c2.116.725 3.664 1.811 3.36 3.832zm-5.928-.106l-.92 3.668c1.136.28 4.64 1.399 5.159-.67zm1.256-5.006l-.835 3.318c.946.234 3.863 1.187 4.336-.69z">
															</path>
														</g>
													</g>
												</svg>
												<strong>Ada</strong>
											</div>
										</td>
										<td>336.99</td>
										<td>
											<div class="rate negative">
												<i class="icon-arrow-up"></i>
												<span>6.84%</span>
											</div>
										</td>
									</tr>
									<tr>
										<td>
											<div class="name">
												<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 30 30">
													<g>
														<g clip-path="url(#clip-005E2401-079E-1234-50F1-94958D2086FA)" opacity=".9">
															<path fill="#f7931a"
																d="M29.548 18.629c-2.003 8.036-10.142 12.926-18.18 10.922C3.336 27.547-1.554 19.408.45 11.373 2.452 3.336 10.591-1.555 18.625.45c8.036 2.003 12.926 10.144 10.923 18.18">
															</path>
														</g>
														<g opacity=".9">
															<path fill="#fff"
																d="M19.357 15.558c1.504.778 2.269 1.971 1.54 4.04-.905 2.57-3.054 2.787-5.912 2.25l-.694 2.763-1.676-.415.685-2.727a63.298 63.298 0 0 1-1.336-.344l-.687 2.74-1.674-.416.694-2.769c-.392-.1-.79-.206-1.195-.307l-2.182-.54.833-1.907s1.234.326 1.217.302c.475.117.685-.191.769-.396l1.096-4.368.177.043a1.373 1.373 0 0 0-.174-.055l.782-3.118c.02-.355-.103-.801-.782-.97.027-.017-1.216-.3-1.216-.3l.445-1.78 2.312.574-.002.008c.348.086.706.168 1.07.25l.687-2.736 1.675.415-.673 2.683c.45.102.903.205 1.343.314l.668-2.665 1.677.415-.687 2.737c2.116.725 3.664 1.811 3.36 3.832zm-5.928-.106l-.92 3.668c1.136.28 4.64 1.399 5.159-.67zm1.256-5.006l-.835 3.318c.946.234 3.863 1.187 4.336-.69z">
															</path>
														</g>
													</g>
												</svg>
												<strong>Ada</strong>
											</div>
										</td>
										<td>336.99</td>
										<td>
											<div class="rate positive">
												<i class="icon-arrow-up"></i>
												<span>6.84%</span>
											</div>
										</td>
									</tr>
								</table>
							</div>
						</div>
					</div>
				</div>
			</form>
		</div>
	</div>
</template>

<script>
	import Vue from 'vue'

	var blogURL = 'https://html-cafe.com/out/crypto-portal/contentJSON.json'

	export default {
		data: function () {
			return {
				tradingAccordionNavigation: asideAccordionItems
			}
		},
		mounted() {
			selectCustom();
		},
		updated(){
			customScroll();
		},
		created: function(){
			this.fetchData();
			
		},
		methods: {
			//accordion
			showHideSector: function(event) {
				event.target.classList.toggle("active");
				
				var sector = event.target.nextElementSibling;
				
				if (sector.style.maxHeight) {
					sector.style.maxHeight = null;
				} else {
					sector.style.maxHeight = sector.scrollHeight + "px";
				}
			},
			fetchData: function(){
				var xhr = new XMLHttpRequest();
				xhr.open('GET', blogURL);
				xhr.onload = function(){
					const contentObj = JSON.parse(xhr.responseText);
					contentObj.asideAccordionList.forEach(e => {
						asideAccordionItems.push(asideAccordionCore(e.name, e.num));
					});
				}
				xhr.send();
			}
		}
	}

	//funcrions core
	function asideAccordionCore(name, num) {
		return {
			name,
			num
		}
	}

	const asideAccordionItems = [];

	new Vue({
		data: {
			tradingAccordionNavigation: asideAccordionItems
		}
	});

	// functions --
	//select custom
	function selectCustom() {
		var x, i, j, l, ll, selElmnt, a, b, c;
		/*look for any elements with the class "custom-select":*/
		x = document.getElementsByClassName("custom-select");
		l = x.length;
		for (i = 0; i < l; i++) {
			selElmnt = x[i].getElementsByTagName("select")[0];
			ll = selElmnt.length;
			/*for each element, create a new DIV that will act as the selected item:*/
			a = document.createElement("DIV");
			a.setAttribute("class", "select-selected");
			a.innerHTML = selElmnt.options[selElmnt.selectedIndex].innerHTML;
			x[i].appendChild(a);
			/*for each element, create a new DIV that will contain the option list:*/
			b = document.createElement("DIV");
			b.setAttribute("class", "select-items select-hide");
			for (j = 1; j < ll; j++) {
				/*for each option in the original select element,
				create a new DIV that will act as an option item:*/
				c = document.createElement("DIV");
				c.innerHTML = selElmnt.options[j].innerHTML;
				c.addEventListener("click", function () {
					/*when an item is clicked, update the original select box,
					and the selected item:*/
					var y, i, k, s, h, sl, yl;
					s = this.parentNode.parentNode.getElementsByTagName("select")[0];
					sl = s.length;
					h = this.parentNode.previousSibling;
					for (i = 0; i < sl; i++) {
						if (s.options[i].innerHTML == this.innerHTML) {
							s.selectedIndex = i;
							h.innerHTML = this.innerHTML;
							y = this.parentNode.getElementsByClassName("same-as-selected");
							yl = y.length;
							for (k = 0; k < yl; k++) {
								y[k].removeAttribute("class");
							}
							this.setAttribute("class", "same-as-selected");
							break;
						}
					}
					h.click();
				});
				b.appendChild(c);
			}
			x[i].appendChild(b);
			a.addEventListener("click", function (e) {
				/*when the select box is clicked, close any other select boxes,
				and open/close the current select box:*/
				e.stopPropagation();
				closeAllSelect(this);
				this.nextSibling.classList.toggle("select-hide");
				this.classList.toggle("select-arrow-active");
			});
		}
		function closeAllSelect(elmnt) {
			/*a function that will close all select boxes in the document,
			except the current select box:*/
			var x, y, i, xl, yl, arrNo = [];
			x = document.getElementsByClassName("select-items");
			y = document.getElementsByClassName("select-selected");
			xl = x.length;
			yl = y.length;
			for (i = 0; i < yl; i++) {
				if (elmnt == y[i]) {
					arrNo.push(i)
				} else {
					y[i].classList.remove("select-arrow-active");
				}
			}
			for (i = 0; i < xl; i++) {
				if (arrNo.indexOf(i)) {
					x[i].classList.add("select-hide");
				}
			}
		}
		/*if the user clicks anywhere outside the select box,
		then close all select boxes:*/
		document.addEventListener("click", closeAllSelect);
	}

	//custom scroll
	function customScroll() {
		(() => {
			// should we register the wakey wakey fix
			const wakeyFixRequired =
				"CSS" in window &&
				typeof CSS.supports === "function" &&
				!CSS.supports("-webkit-appearance", "none");

			const ROOT_CLASS = "scrollscreen";

			const createElement = (tag, name) => {
				const el = document.createElement(tag);
				el.className = `${ROOT_CLASS}--${name}`;
				return el;
			};

			const createScrollscreen = (root) => {
				const fragment = document.createDocumentFragment();
				[...root.childNodes].forEach((child) => {
					fragment.appendChild(child);
				});

				const content = createElement("div", "content");
				content.appendChild(fragment);
				root.appendChild(content);

				const track = createElement("div", "track");
				root.appendChild(track);

				const slider = createElement("div", "slider");
				track.appendChild(slider);

				let pendingFrame = null;

				const redraw = () => {
					cancelAnimationFrame(pendingFrame);

					pendingFrame = requestAnimationFrame(() => {
						const contentHeight = content.scrollHeight;
						const containerHeight = root.offsetHeight;
						const percentageVisible = containerHeight / contentHeight;
						const sliderHeight = percentageVisible * containerHeight;
						const percentageOffset =
							content.scrollTop / (contentHeight - containerHeight);
						const sliderOffset = percentageOffset * (containerHeight - sliderHeight);

						track.style.opacity = percentageVisible === 1 ? 0 : 1;

						slider.style.cssText = `
						height: ${sliderHeight}px;
						transform: translateY(${sliderOffset}px);
					`;
					});
				};

				// need to update if window is resized or if container is scrolled
				[...root.childNodes].forEach((child) => {
					child.addEventListener("click", redraw);
				});
				content.addEventListener("scroll", redraw);
				window.addEventListener("load", redraw);
				window.addEventListener("resize", redraw);

				// first redraw
				redraw();

				// if we don't need to do the wakey wakey fix we done
				if (!wakeyFixRequired) {
					return;
				}

				// the wakey wakey function quickly scrolls the contents so Firefox enables the scrollbar and the user can drag it
				const wakey = () => {
					requestAnimationFrame(() => {
						const offset = content.scrollTop;
						content.scrollTop = offset + 1;
						content.scrollTop = offset;
					});
				};

				// wake up scrollbars on MacOS Firefox
				root.addEventListener("mouseenter", wakey);

				// trigger so it's drawn correctly for the first time
				wakey();
			};

			// create scrollies
			[...document.querySelectorAll(`.${ROOT_CLASS}`)].forEach(createScrollscreen);
		})();
	}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/variables";
@import "../styles/mixins";
@import "../styles/media-queries";

.sub_heading{
	display: flex;
	padding: 8px 18px;
	margin: 0 -4px;
	flex-shrink: 0;
	flex-grow: 0;
	border-bottom: 1px solid rgba(55, 67, 79, .3);
	.col{
		width: 60%;
		padding: 0 4px;
		&.second{
			width: 40%;
		}
	}
}

//search form
.wrap_input{
	border-radius: 8px;
	border: 1px solid #37434f;
	background-color: #232d38;
	display: flex;
	.input{
		border: none;
		background: none;
		border-radius: 0;
	}
}
.input{
	background-color: #232d38;
	border: 1px solid #37434f;
	border-radius: 8px;
	width: 100%;
	flex-shrink: 1;
	flex-grow: 1;
	min-width: 1px;
	height: 34px;
	color: #9faab7;
	padding: 10px 14px;
	font-family: 'Roboto', sans-serif;
	letter-spacing: 0.6px;
	font-size: 14px;
	line-height: 1.2;
	@include max-screen(1440px) {
		font-size: 13px;
	}
	&.single{
		border-radius: 8px;
		border: 1px solid #37434f;
		background-color: #232d38;
	}
}
.btn_search{
	background-color: #37434f;
	color: #fff;
	font-size: 14px;
	font-weight: 500;
	letter-spacing: 0.6px;
	border: none;
	padding: 0 8px;
	border-radius: 0 7px 7px 0;
	cursor: pointer;
	text-transform: uppercase;
	@include max-screen(1440px) {
		font-size: 13px;
	}
	i{
		font-size: 14px;
	}
}

//accordion
.aside_accordion{
	background-color: #303b4d;
	display: flex;
	flex-direction: column;
}
.accordion_heading{
	// padding: 0 20px;
	flex-shrink: 0;
	flex-grow: 0;
	table{
		width: 100%;
		border-collapse: collapse;
		color: #bfcefb;
		font-size: 15px;
	}
	th{
		font-weight: 700;
		// padding: 13px 0;
		padding: 13px 20px;
		width: 25%;
		text-align: right;
		&:first-child{
			width: 50%;
			text-align: left;
		}
	}
}
.accordion_content{
	flex-shrink: 1;
	flex-grow: 1;
	min-height: 1px;
	position: relative;
	.scrollscreen{
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
	}
	.button{
		background-color: #303b4d;
		border: none;
		width: 100%;
		text-align: left;
		display: flex;
		align-items: center;
		font-size: 15px;
		line-height: 1.2;
		color: #fff;
		padding: 12px 20px;
		cursor: pointer;
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
			z-index: 2;
		}
		strong,
		em{
			margin-right: 10px;
		}
		&.active{
			i{
				transform: rotate(0);
			}
		}
		i{
			color: #788797;
			font-size: 14px;
			transform: rotate(-90deg);
		}
	}
	.hidden{
		// display: none;
		max-height: 0;
		overflow: hidden;
		transition: max-height 0.2s ease-out;
	}
	table{
		background-color: #303b4d;
		width: 100%;
		border-collapse: collapse;
	}
	tr{
		&:nth-child(2n){
			td{
				background-color: #232d38;
			}
		}
		@include min-screen(1025px) {
			&:hover{
				td{
					background-color: rgba(216, 216, 216, .25);
				}
			}
		}
	}
	td{
		background-color: #202a34;
		padding: 10px 20px;
		width: 25%;
		text-align: right;
		&:first-child{
			width: 50%;
			text-align: left;
		}
	}
	.name{
		display: flex;
		align-items: center;
		text-transform: uppercase;
		svg{
			flex-shrink: 0;
			flex-grow: 0;
			margin-right: 10px;
		}
	}
	.rate{
		display: flex;
		align-items: center;
		span{
			margin-left: 5px;
		}
		i{
			font-size: 10px;
		}
		&.positive{
			color: #56e39e;
		}
		&.negative{
			color: #ff5353;
			i{
				transform: rotate(180deg);
			}
		}
	}
}

</style>
