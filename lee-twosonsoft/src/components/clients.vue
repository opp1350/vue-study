<template>
	<div class="clientsWrap">
		<div class="clientsItemWrap">
			<div class="clientsItem titleWrap">
				<h2 class="Title">Our Clients</h2>
				<p class="subTitle">두손소프트는 국내 유수기업의 사업컨설팅과 함께 신규사업,
				개발사업, 혁신사업 등 다양한 프로젝트 구축 경험이 있습니다.</p>
				<div class="btnWrap">
					<span>...end you!</span><button type="button" class="borderBtn">프로젝트 문의</button>
				</div>
			</div>
			<div class="clientsItem content">
				<ul class="clientsList floatClear">
					<li class="clientsListItems" v-for="item in items" :key="item.key"><img :src="item.img" :alt="item.imgAlt"></li>
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
					img: require('@/assets/img/lotte_grey_70.png'),
					imgAlt: 'lotte'
				},
				{
					img: require('@/assets/img/cjHello_grey_70.png'),
					imgAlt: 'cjHello'
				},
				{
					img: require('@/assets/img/ss_grey_70.png'),
					imgAlt: '삼성생명'
				},
				{
					img: require('@/assets/img/nh_grey.png'),
					imgAlt: '농협생명'
				},
				{
					img: require('@/assets/img/ss_grey_70.png'),
					imgAlt: '삼성생명'
				},
				{
					img: require('@/assets/img/lotte_grey_70.png'),
					imgAlt: 'lotte'
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
	position: relative;
}
.clientsItem.content {
	flex: 1;
}
.clientsListItems {
	width:33.3332%;
	box-sizing: border-box;
	float:left;
	height: calc(12.25vw - 1.25vw);
	position:relative
}
.clientsListItems img {
	position:absolute;
	top:50%;
	left:50%;
	transform: translate(-50%,-50%);
	width:60%;
	max-width:180px;
	height: auto;
}
.btnWrap {
	position: absolute;
	bottom:0;
	right:0
}
.btnWrap span {
	color:#777;
	margin-right: 10px
}
</style>
