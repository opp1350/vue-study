<template>
	<div class="NewsWrap">
		<div class="NewsItemWrap">
			<div class="right">
				<div class="rightNewsItems">
					<div class="titleWrap">
						<h2 class="title">News</h2>
						<p># 두손스토리</p>
						<p># IT News</p>
					</div>
					<div class="contWrap">
						<h4 class="title">에델마을 방문 기부금 전달</h4>
						<p class="date">2017 / 08 / 30</p>
						<p class="content">지난 16일 SI사업부 배재성 과장과 경영지원실 이아람 대리가 두손소프트 대표로 서울시 구로구 천왕동에 위치한 에델마을을 찾아 기부금 전달을 하고 왔습니다.</p>
					</div>
					<button type="button" class="borderBtn newsBtn">뉴스 더보기</button>		
				</div>
			</div>
			<div class="left">
				<div class="leftNewsItems" v-for="item in items" :key="item.key">
					<div class="titleWrap">
						<h4 class="title">{{ item.title }}</h4>
						<p class="date-b">{{ item.date }}</p>
						<a v-bind:href="item.link" title="더 자세히 보기" target="_blank" class="newsLink">더 자세히 보기<span class="arrow"></span></a>
					</div>
						<p class="hashtag">{{ item.hashtag }}</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'mainNews',
	data () {
		return {
			items: [
				{
					title:'저작권 등록증',
					date:'2017 / 08 / 30',
					hashtag:'#두손스토리',
					link:'http://www.twosonsoft.com/news/news_sub01.do?menuType=2&listNum=287'
				},
				{
					title:'IoT 보안, 헬스케어 분야로 확장.. 특화 테스트 환경 마련',
					date:'2017 / 08 / 30',
					hashtag:'#IT News',
					link:'http://www.twosonsoft.com/news/news_sub01.do?menuType=2&listNum=286'
				},
			]
		}
	}
}
</script>

<style scoped>
.NewsWrap {
	margin-bottom:100px
}
.NewsItemWrap {
	display: flex
}
.right {
	flex:1;
	background:url('../assets/img/newsBg01.png') 55% bottom no-repeat;
	background-size: cover
}
.rightNewsItems {
	background: linear-gradient(to top, rgba(73,73,105,0.8), rgba(255,255,255,0));
	position:relative;
	height: 100%;
	width:100%;
	color:#fff;
	padding: 5vw;
	box-sizing: border-box
}
.rightNewsItems .titleWrap {
	position: absolute;
	bottom: 5vw;
	display: inline-block
}
.rightNewsItems .titleWrap .title {
	font-size: 60px;
	margin-bottom:20px
}
.rightNewsItems .titleWrap p {
	line-height: 24px
}
.rightNewsItems .contWrap {
	position: absolute;
	bottom: 5vw;
	width:35%;
	right:5vw
}
.rightNewsItems .contWrap p {
	line-height: 24px
}
.rightNewsItems .contWrap p.date {
	font-size: 12px;
	color:rgba(255,255,255,0.6);
	margin-bottom:5px
}
.rightNewsItems .contWrap .title {
	font-size:16px;
	margin-bottom: 10px
}
.newsBtn {
	position: absolute;
	right:calc(35% + 5vw - 130px);
	cursor:pointer
}
.rightNewsItems p {
	font-weight: 300
}
.left {
	display: flex;
	flex-direction: column;
	width:calc(25vw - 1.25vw);
}
.leftNewsItems {
	width:100%;
	height: calc(25vw - 1.25vw);
	box-sizing: border-box;
	position: relative;
	padding:2vw;
}
.leftNewsItems:first-of-type {
	background: #fff
}
.leftNewsItems:nth-of-type(2) {
	background: #e6e6e6
}
.leftNewsItems div.titleWrap {
	position:absolute;
	width:calc(100% - 5vw);
}
.leftNewsItems div.titleWrap .title {
	margin-bottom:10px
}
.leftNewsItems p.hashtag {
	position: absolute;
	bottom:2.5vw;
	right:2.5vw
}
a.newsLink {
	position: relative;
	opacity:0;
	margin-top:10px
}
span.arrow {
	width:25px;
	height:12px;
	position: absolute;
	bottom:0;
	margin-left:5px;
	background: url("../assets/img/arrow.png") 0 0 no-repeat;
	background-size: contain;
	opacity:1
}
</style>
