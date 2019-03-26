<template>
	<div class="clientsWrap">
		<div class="clientsItemWrap">
			<div class="clientsItem titleWrap">
				<h2 class="Title">Our Clients</h2>
				<p class="subTitle">두손소프트는 국내 유수기업의 사업컨설팅과 함께 신규사업,<br>
				개발사업, 혁신사업 등 다양한 프로젝트 구축 경험이 있습니다.</p>
			</div>
			<div class="clientsItem content">
				<ul class="clientsList floatClear">
					<li class="clientsListItems" v-for="item in items" :key="item.key"><img src="" alt=""></li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'mainclients',
	data () {
		return {
			items: [
				{
				
				},
				{
				
				},
				{
				
				},
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
.clientsWrap {
	margin-bottom:100px
}
.clientsItemWrap {
	display: flex
}
.clientsItem.titleWrap {
	flex-direction: column;
	width:25%;
	border:1px solid darkcyan
}
.clientsItem.content {
	flex: 1;
	border:1px solid darkorchid
}
.clientsListItems {
	width:33.3332%;
	border: 1px dashed darkorange;
	box-sizing: border-box;
	float:left;
	height: calc(12.25vw - 1.25vw);
}
</style>
