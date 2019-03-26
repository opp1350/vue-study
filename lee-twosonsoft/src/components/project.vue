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
						</a>
					</div>
				</div>
				<div class="projectContRight">
					<div class="projectContRightItem">
						<a href="#none" class="rightInner">
							<div class="projectConrRightItemName">
							</div>		
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
				},
				{
					titleBold: '삼성생명',
					titleNormal: 'GA 모바일 시스템 구축',
					link:'https://www.google.co.kr/?hl=ko',
				},
				{
					titleBold: '삼성생명',
					titleNormal: 'GFC 기업분석보고서',
					link:'https://www.youtube.com/?gl=KR&hl=ko',
				},
				{
					titleBold: '신한생명',
					titleNormal: '모바일 계약서류 발송 시스템 구축',
					link:'https://www.apple.com/',
				},
			]
		}
	}
}
</script>

<style scoped>
.projectWrap {
	margin-bottom:2.5vw
}
.titleWrap {
	margin-bottom: 10px
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
	background:none;
	transition: 0.3s all;
	display:block;
	width:100%;
	height:100%
}
.rightInner:hover {
	background: linear-gradient(to top, #1E1E47, rgba(255,255,255,0))
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
	font-weight: bold
}
.projectContLeftItem {
	float: left;
	width: 50%;
	height: calc(25vw - 1.25vw);
	box-sizing: border-box
}
</style>
