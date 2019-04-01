<template>
	<div class="sliderAllWrap swiper-container">
		<div class="imgsliderWrap swiper-wrapper">
			<div class="imgSlider swiper-slide">
				<div class="imgSliderInner">
					<div class="sliderTopList floatClear">
						<ul>
							<li>SI & SM 사업(기술용역)</li>
							<li>개발 사업</li>
							<li>디자인 및 퍼블리싱 사업</li>
							<li>IT 컨설팅 사업</li>	
						</ul>
						<ul>
							<li>RIA 전문개발회사</li>
							<li>컨설팅 및 IT Infra 구축</li>
							<li>Software Development</li>
						</ul>
					</div>
					<div class="sliderBottomText floatClear">
						<h2 class="title">
							<span>ABOUT</span>
							<span>US</span>
						</h2>
						<p class="content">두손소프트는 국내 유수기업의 사업컨설팅과 함께 신규사업, 개발사업, 혁신사업 등 다양한 프로젝트 구축 경험이 있습니다.</p>
					</div>
					<div class="rotationText">
						<p>회사소개</p>
						<p>TwoSonSoft</p>
					</div>
				</div>
			</div>
			<div class="imgSlider swiper-slide">
				<div class="imgSliderInner">
					<div class="sliderTopList floatClear">
						<ul>
							<li>SI & SM 사업(기술용역)</li>
							<li>개발 사업</li>
							<li>디자인 및 퍼블리싱 사업</li>
							<li>IT 컨설팅 사업</li>	
						</ul>
						<ul>
							<li>RIA 전문개발회사</li>
							<li>컨설팅 및 IT Infra 구축</li>
							<li>Software Development</li>
						</ul>
					</div>
					<div class="sliderBottomText floatClear">
						<h2 class="title">
							<span>TEST</span>
							<span>CONTENT</span>
						</h2>
						<p class="content">또한 다우기술, 어도비, 마이크로소프트 등의 기술파트너로서 다양한 프로젝트의 수주와 개발완수를 위해서 두손이 두발로 뛰고 있습니다.</p>
					</div>
					<div class="rotationText">
						<p>비지니스</p>
						<p>TwoSonSoft</p>
					</div>
				</div>
			</div>
		</div>
		<!-- If we need pagination
		<div class="swiper-pagination"></div> -->
		<!-- If we need navigation buttons -->
		<div class="swiper-button-prev swiper-button-white custom"></div>
		<div class="swiper-button-next swiper-button-white custom"></div>
	</div>
</template>
<script>
export default {
	name: 'mainSlide',
	props: {
	}
}
</script>

<style scoped>
.custom {
	width:15px;
	height:22px;
	margin-top:0;
	background-size: 15px 22px;
	top:calc(50vh + 30px)
}
.sliderAllWrap {
	width:100%;
	height: auto;
}
.imgsliderWrap {
	width:100%;
	height: inherit;
} 
.imgSlider {
	width:100%;
	height: 800px;
	color:#fff;
}
.imgSlider:first-of-type {
	background: url("../assets/img/main-slider-img01-1920.jpg") 50% 50% no-repeat;
	background-size: cover;
}
.imgSlider:nth-of-type(2) {
	background: url("../assets/img/main-slider-img-1920.jpg") 50% 50% no-repeat;
	background-size: cover;
}
.imgsliderWrap {
	width:100%;
	height: inherit;
} 
.imgSliderInner {
	padding:80px 2.5vw 0;
	box-sizing:border-box;
	position:relative;
	width: 100%;
	height: 100%;
	background:rgba(0,0,0,0.6);
}
.sliderTopList {
	font-weight: 300;
	position: absolute;
	top: calc(80px + 5vw);
	left: 5vw
}
.sliderTopList ul {
	float: left;
	margin-left: 5vw
}
.sliderTopList ul:first-child {
	margin-left: 0
}
.sliderTopList ul li {
	margin-bottom:5px;
} 
.sliderTopList ul li:last-child {
	margin-bottom:0
}
.sliderBottomText {
	position: absolute;
	bottom:5vw;
	left:5vw;
	width:calc(100% - 10vw)
}
.sliderBottomText .title {
	float: left;
	font-size: 90px;
	font-weight: 900;
	line-height: 72px;
	position: relative;
}
.sliderBottomText .title span {
	display: block
}
.sliderBottomText .title span:first-child {
	margin-bottom:5px
}
.sliderBottomText .content {
	float: right;
	width:25vw;
	font-weight: 300;
	line-height: 24px;
	margin-top:101px;
	text-align: justify;
	word-break: break-all;
	position:absolute;
	bottom:0;
	right:0
}
.rotationText {
	position: absolute;
	right:5vw;
	top: calc(80px + 5vw + 14px);
}
.rotationText p {
	font-weight: 300;
	display:block;
	margin-bottom:calc(50vh - 80px - 5vw);
	text-align: right;
	transform: rotate(90deg);
	margin-right: -25px
}
</style>
