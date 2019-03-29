<template>
	<div class="footer">
		<div class="inner floatClear">
			<div class="left fL">
				<ul class="footerMenu">
					<li v-for="item in footerList" :key="item.key">
						<a v-bind:href="item.link" target="_blank">
							{{item.list}}
						</a>
					</li>
				</ul>
				<p class="copyRight">TWOSONSOFT. All Rights Reserved</p>
			</div>
			<div class="right fR">
				<p v-for="item in footerItems" :key="item.key">{{item.info}}</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'mainFooter',
	data () {
		return {
			footerItems: [
				{
					info:'주소 : 서울특별시 구로구 디지털로26길 111 JNK디지털타워 502호'
				},
				{
					info:'대표이사 : 손영대'
				},
				{
					info:'전화 : 02-3461-8686 팩스 : 070-8677-5460 이메일 : twosonsoft@twosonsoft.com'
				},
			],
			footerList : [
				{
					 list: '프로젝트 문의',
					 link: 'https://www.naver.com/'
				},
				{
					 list: '입사지원',
					 link: 'https://www.google.co.kr/?hl=ko'
				},
				{
					 list: '회사소개서 받기',
					 link: 'https://www.youtube.com/?gl=KR&hl=ko'
				}
			]
		}
	}
}
</script>

<style scoped>
* {
	line-height: 24px;
	font-size: 12px
}
.footer {
	background:#EEEEF2;
	padding:40px 0 30px
}
.inner {
	padding:0 2.5vw;
	color:#777;
}
ul {
	margin-bottom:30px
}
li {
	display: inline-block;
	margin-right: 20px
}
li:last-child {
	margin-right:0
}
.right {
	text-align: right
}
a {
	color:#777
}
a:hover {
	text-decoration: underline;
	color:#333
}
</style>
