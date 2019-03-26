<template>
	<div class="NewsWrap">
		<div class="NewsItemWrap">
			<div class="right">

			</div>
			<div class="left">
				<div class="leftNewsItems">
					<a href="#none" title="더 자세히 보기">
						<h4>제목</h4>
						<p>날짜</p>
						<p class="hashtag">두손스토리</p>
					</a>
				</div>
				<div class="leftNewsItems">
					<a href="#none" title="더 자세히 보기">
						<h4>제목</h4>
						<p>날짜</p>
						<p class="hashtag">두손스토리</p>
					</a>
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
				
				},
				{
				
				},
				{
				
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
	background-color:darkslategray 
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
}
.leftNewsItems:first-of-type {
	background: #fff
}
.leftNewsItems:nth-of-type(2) {
	background: #e6e6e6
}
.leftNewsItems a {
	display: block;

} 
</style>
