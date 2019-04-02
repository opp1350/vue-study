<template>
	<div class="solutionWrap">
		<div class="solutionItemWrap">
			<div class="solutionItem titleWrap">
				<h2 class="Title">Solution</h2>
				<p class="subTitle">두손소프트 솔루션 - Non-ActiveX, Non-Plugin</p>
			</div>
			<div class="solutionItem content bg" v-for="item in items" :key="item.key">
				<h4 class="solutionItemTitle">{{ item.title }}</h4>
				<p class="solutionItemCont">{{ item.content1st }}</p>
				<p class="solutionItemCont">{{ item.content2nd }}</p>
				<a class="goToPilot" v-bind:href="item.link" target="_blank">체험하러가기<span class="arrow"></span></a>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'mainSolution',
	data () {
		return {
			items: [
				{
					title: 'Web FC Note',
					content1st:'어떠한 프로그램도 설치할 필요 없는 HTML5 기반의 100% Pure Web 필기 메모 컴포넌트 제품입니다.',
					content2nd:'자동차 사고시 현장에 출동하여 사고조사 및 처리업무 , 긴박한 현장 정보들을 사진이미지와 함께 빠르게 필기 메모가 가능합니다. 작성된 메모들은 업무프로그램안에서 관리되어 필요시 언제 어느기기에서나 열람/사용할 수 있습니다.',
					link:'http://www.twosonsoft.com/solution/pilot_fcnote.do',
				},
				{
					title: 'PDF Web Viewer',
					content1st:'TS PDF Web Viewer는 계약, 신청, 약관확인 등의 다양한 페이퍼리스 시스템에서 PDF 출력을 담당하는 뷰어 솔루션으로서 100% 웹기반으로 다양한 사용자 환경에서 빠른 열람이 가능합니다. ',
					content2nd:'보험사, 카드사, 은행, 공공에 이어 의료, 제조, 유통, 서비스 등 전 산업분야에서 활용, 확산되고 있습니다.',
					link:'http://www.twosonsoft.com/solution/sol_pdf.do',
				},
				{
					title: 'Web Scanner',
					content1st:'기울어진 이미지를 반듯하고 뚜렷하게 !',
					content2nd:'TS Web Scanner는 신분증 제출, 영수증 전표처리, 계약서 스캔/전송 등의 오프라인 문서업무에서 쉽고 간편하게 정리된 이미지로 아날로그 문서를 디지털 문서로 스캔처리 솔루션으로 모바일, 웹 기반의 다양한 페이퍼리스 시스템의 주요 입력 기능으로 활용되고 있습니다. ',
					link:'http://www.twosonsoft.com/solution/sol_scanner.do',
				},
			]
		}
	}
}
</script>

<style scoped>
.solutionWrap {
	margin:100px auto;
}
.solutionItemWrap {
	display: flex;
}
.solutionItem {
	flex-direction: column;
	width:25%;
}
.solutionItem.content {
	min-height:calc(25vw - 1.25vw);
	box-sizing: border-box;
	padding:2.5vw;
	transition: 0.3s all;
	color:#333;
	text-align: justify;
	word-break: break-all;
	cursor: default;
	position: relative;
}
.solutionItemCont {
	line-height: 24px
}
.solutionItem.content:hover {
	background-color: #fff;
}
.solutionItem.content:hover a.goToPilot {
	color:rgba(100,100,100,1);
}
.solutionItem.content a.goToPilot {
	color:rgba(100,100,100,0);
	transition: 0.3s all;
	position: absolute;
	bottom:2.5vw;
}
.solutionItem.content a.goToPilot:hover {
	color:#000;
}
span.arrow {
	width:25px;
	height:12px;
	position: absolute;
	bottom:0;
	margin-left:5px;
	background: url("../assets/img/arrow.png") 0 0 no-repeat;
	background-size: contain;
	opacity:0
}
h4.solutionItemTitle {
	font-size: 30px;
	margin-bottom:50px
}
.solutionItemCont:first-of-type {
	margin-bottom:10px
}
.solutionItemCont:last-of-type {
	padding-bottom: 50px
}
.bg:nth-of-type(2) {
	background-image: url("../assets/img/1.png");
	background-position: 90% 100%;
	background-repeat: no-repeat
}
.bg:nth-of-type(3) {
	background-image: url("../assets/img/2.png");
	background-position: 90% 100%;
	background-repeat: no-repeat
}
.bg:last-of-type {
	background-image: url("../assets/img/3.png");
	background-position: 90% 100%;
	background-repeat: no-repeat
}
.bg:nth-of-type(2):hover {
	background-image: url("../assets/img/1_hover.png");
}
.bg:nth-of-type(3):hover {
	background-image: url("../assets/img/2_hover.png");
}
.bg:last-of-type:hover {
	background-image: url("../assets/img/3_hover.png");
}
@media screen and (max-width:950px) {
	.solutionItemCont:nth-of-type(2) {
		display: none
	}
	.bg:nth-of-type(2),.bg:nth-of-type(3),.bg:last-of-type {
		background-position: 100% 45%;
	}
}
@media screen and (max-width:1260px) {
	.solutionWrap {
		margin:70px auto;
	}
	.solutionItemWrap {
		display: block
	}
	.solutionItemWrap:after {
		content: "";
		display: block;
		clear: both;
	}
	.solutionItem.titleWrap {
		width:100%;
		margin-bottom: 2.5vw
	}
	.solutionItem.content {
		float: left;
		width:33.3332%;
		min-height:calc(33vw - 1.25vw);
	}
}
</style>
