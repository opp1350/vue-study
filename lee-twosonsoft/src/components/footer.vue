<template>
	<div class="footer">
		<div class="inner floatClear">
			<div class="left fL">
				<ul class="footerMenu">
					<li><a href="#none">{{}}</a></li>
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
			]
		}
	}
}
</script>

<style scoped>
.footer {
	background:#EEEEF2;
	padding:50px 0 30px
}
.inner {
	/* max-width: 1920px;
	margin:0 auto; */
	padding:0 2.5vw
}
.right {
	text-align: right
}
</style>
