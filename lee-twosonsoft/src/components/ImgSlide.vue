<template>
	<div class="imgsliderWrap">
		<div class="imgSlider"></div>
	</div>
</template>

<script>
export default {
	name: 'mainSlide',
	props: {
	}
}
</script>

<style scoped>
.imgSlider {
	width:100%;
	height: 900px;
	background:rgba(0,0,0,0.6)
}
.imgsliderWrap {
	width:100%;
	height: inherit;
	background: url("../assets/img/main-slider-img-1920.jpg") 50% 50% no-repeat;
	background-size: cover
} 
</style>
