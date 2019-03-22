<template>
	<div class="projectWrap">
		<div class="projectItemWrap">
			<div class="titleWrap floatClear">
				<h2 class="Title">Project</h2>
				<a href="#none" class="subTitle fR">프로젝트 더보기</a>
			</div>
			<div class="projectContWrap">
				<div class="projectContLeft">
					<div class="projectContLeftItem" v-for="item in items" :key="item.key">
						<div class="inner">
							<div class="projectContLeftItemName">
								<p class="bold">{{ item.titleBold }}</p>
								<p class="normal">{{ item.titleNormal }}</p>
							</div>
						</div>
					</div>
				</div>
				<div class="projectContRight">
					<div class="projectContRightItem">
						<div class="projectConrRightItemName">
							<h1>rightBox</h1>
						</div>					
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
					titleBold: 'NICE평가정보 ―',
					titleNormal: 'NICE TCB 모바일 서비스 구축',
				},
				{
					titleBold: 'NICE평가정보 22―',
					titleNormal: 'NICE TCB 모바일 서비스 구축22',
				},
				{
					titleBold: 'NICE평가정보 33―',
					titleNormal: 'NICE TCB 모바일 서비스 구축33',
				},
				{
					titleBold: 'NICE평가정보 44―',
					titleNormal: 'NICE TCB 모바일 서비스 구축44',
				},
			]
		}
	}
}
</script>

<style scoped>
.projectWrap {
	margin-bottom:100px
}
.projectContWrap {
	display: flex;
	width:100%;
}
.projectContLeft,
.projectContRight {
	border:1px solid #f0c;
	box-sizing: border-box
}
.projectContLeft {
	width:calc(50vw - 2.5vw);
}
.projectContRight {
	flex: 1
}
.projectContLeftItem {
	float: left;
	width: 50%;
	height: calc(25vw - 1.25vw);
	border:1px solid #515151;
	box-sizing: border-box
}
</style>
