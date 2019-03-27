<template>
	<div class="gnb">
		<div class="inner">
			<h1 class="mainLogo">
				<img src="../assets/img/mainLogo.png" alt="twosonsoft" class="default">
				<img src="../assets/img/mainLogoBlack.png" alt="twosonsoft" class="black">
			</h1>
			<ul>
				<li v-for="el in items" :key="el.key"><a href="#none">{{ el.li }}</a></li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: 'mainGnb',
	data () {
		return {
			items : [
				{
					li:"Business"
				},
				{
					li:"Portfolio"
				},
				{
					li:"Solution"
				},
				{
					li:"News"
				},
				{
					li:"About Us"
				},
				{
					li:"Contact Us"
				},
				
			]
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.gnb {
	width:100%;
	height: 80px;
	position:fixed;
	z-index: 100;
	top:0
}
.inner::after {
	content: "";
	display: block;
	clear: both;
}
.gnb .inner {
	/* max-width: 1920px;
	margin:0 auto; */
	padding:0 2.5vw;
	height: 100%;
	border-bottom:1px solid rgba(255,255,255,0.4)
}
.gnb h1 {
	float: left;
	width:135px;
	display: block;
	height: inherit;
}
.gnb h1 img {
	width:130px;
	position:absolute;
	top:50%;
	transform: translateY(-50%);
	display:none
}
.gnb h1 img.show {
	display:block
}
ul {
	list-style-type: none;
	float: right;
	padding:30px 0
}
li {
	display: inline-block;
	margin-right: 60px;
}
li:last-child {
	margin-right: 0;
}
.gnb a {
	font-weight: 300;
	color: rgba(255,255,255,0.6);
	text-decoration: none;
	transition: 0.3s all
}
.gnb a:hover {
	color: rgba(255,255,255,1);
}
</style>
