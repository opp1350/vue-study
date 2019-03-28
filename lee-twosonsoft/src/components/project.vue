<template>
	<div class="projectWrap">
		<div class="projectItemWrap">
			<div class="titleWrap floatClear">
				<h2 class="Title fL">Project</h2>
				<a href="#none" class="subTitle fR">프로젝트 더보기</a>
			</div>
			<div class="projectContWrap">
				<div class="projectContLeft">
					<div class="projectContLeftItem" v-for="item in items" :key="item.key">
						<a class="inner" v-bind:href="item.link" target="_blank">
							<div class="projectContLeftItemName">
								<p class="bold">{{ item.titleBold }}</p>
								<p class="normal">{{ item.titleNormal }}</p>
							</div>
							<div class="projectContLeftItemImg"><img :src="item.img" :alt="item.alt"></div>
						</a>
					</div>
				</div>
				<div class="projectContRight">
					<div class="projectContRightItem">
						<a href="#none" class="rightInner">
							<div class="projectConrRightItemContWrap">
								<h4 class="title">
									<span>삼성생명</span>
									<br>
									<span>모바일 영업지원 시스템 구축</span>
								</h4>
								<p class="date">2018 / 03</p>
								<ul class="content">
									<li>시간과 장소에 상관없이 주요 경영지표를 확인할 수 있는 모바일 경영정보 시스템 구축</li>
									<li>목표대비 미달성 지표에 대한 상시적 모니터링 시스템 구축</li>
								</ul>
							</div>
							<div class="innerBg"></div>		
						</a>				
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'mainproject',
	data () {
		return {
			items: [
				{
					titleBold: 'NICE평가정보',
					titleNormal: 'NICE TCB 모바일 서비스 구축',
					link:'https://www.naver.com/',
					img: require('@/assets/img/port02.png'),
					alt: 'NICE평가정보 NICE TCB 모바일 서비스 구축'
				},
				{
					titleBold: '삼성생명',
					titleNormal: 'GA 모바일 시스템 구축',
					link:'https://www.google.co.kr/?hl=ko',
					img: require('@/assets/img/port03.png'),
					alt: '삼성생명 GA 모바일 시스템 구축'
				},
				{
					titleBold: '삼성생명',
					titleNormal: 'GFC 기업분석보고서',
					link:'https://www.youtube.com/?gl=KR&hl=ko',
					img: require('@/assets/img/port05.png'),
					alt: '삼성생명 GFC 기업분석보고서'
				},
				{
					titleBold: '신한생명',
					titleNormal: '모바일 계약서류 발송 시스템 구축',
					link:'https://www.apple.com/',
					img: require('@/assets/img/port01.png'),
					alt: '신한생명 모바일 계약서류 발송 시스템 구축'
				},
			]
		}
	}
}
</script>

<style scoped>
a {
	color:#333
}
.projectWrap {
	margin-bottom:2.5vw
}
.titleWrap {
	margin-bottom: 1.25vw
}
.subTitle {
	margin-top: 50px
}
.projectContWrap {
	display: flex;
	width:100%;
}
.projectContLeft,
.projectContRight {
	/* border:1px solid #f0c; */
	box-sizing: border-box
}
.projectContLeft {
	width:calc(50vw - 2.5vw);
}
.projectContRight {
	flex: 1;
	background: #9CC7F5
}
.projectContRightItem {
	width:100%;
	height:100%;
	display: block
}
.rightInner {
	display:block;
	width:100%;
	height:100%;
	position: relative;
	padding: 5vw;
	box-sizing: border-box;
	background: url('../assets/img/port04.png') 50% 50% no-repeat;
	background-size: 80%;
}
.rightInner .innerBg {
	position:absolute;
	top:0;
	left:0;
	right:0;
	bottom:0;
	content:"";
	display: block;
	width:100%;
	height:100%;
	background: linear-gradient(to top, rgba(73,73,105,0.8), rgba(255,255,255,0));
}
.rightInner:hover .innerBg {
	background: linear-gradient(to top, rgba(73,73,105,1), rgba(255,255,255,0));	
}
.projectConrRightItemContWrap {
	color:#fff;
	line-height: 24px;
	position: absolute;
	z-index: 1;
	bottom:5vw
}
.projectConrRightItemContWrap 
/* .rightInner:hover {
	background: linear-gradient(to top, rgba(73,73,105,0.8), rgba(255,255,255,0));
} */
h4.title {
	font-size: 16px;
	margin-bottom:10px
}
.date {
	font-size: 12px;
	font-weight: 300;
	color:rgba(255,255,255,0.6);
	margin-bottom: 5px
}
ul.content {
	font-weight: 300
}
ul.content li {
	line-height: 24px
}
a.inner {
	position: relative;
	width:100%;
	height: 100%;
	padding:10%;
	box-sizing: border-box;
	display: block;
	color:#333;
	transition: 0.3s all;
	background: #fff
}
a.inner:hover {
	background: none
}
.projectContLeftItemName {
	position:absolute;
	bottom:10%;
}
p.bold {
	font-weight: bold;
	line-height: 24px
}
p.bold::after {
	content: "―";
	display: inline-block;
	padding-left:5px
}
.projectContLeftItem {
	float: left;
	width: 50%;
	height: calc(25vw - 1.25vw);
	box-sizing: border-box;
	overflow: hidden;
	position:relative;
}
.projectContLeftItemImg {
	position:absolute;
	top:50%;
	left:50%;
	transform: translate(-50%,-50%);
	width:70%;
	transition: 0.3s all
}
.projectContLeftItemImg img {
	width:100%;
	opacity: 0.5;
}
a.inner:hover .projectContLeftItemImg {
	width:73%;
}
/* a.inner:hover .projectContLeftItemImg img {
	opacity: 1;
} */
</style>
