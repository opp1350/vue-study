<template>
	<div id="app">
		<mainGnb/>
		<mainSlide/>
		<div class="appInner">
			<mainSolution/>
			<mainproject/>
			<mainNews/>
			<mainclients/>
		</div>
		<mainFooter/>
	</div>
</template>

<script>
import mainGnb from './components/MainMenu.vue'
import mainSlide from './components/ImgSlide.vue'
import mainSolution from './components/Solution.vue'
import mainproject from './components/project.vue'
import mainFooter from './components/footer.vue'
import mainNews from './components/News.vue'
import mainclients from './components/clients.vue'
import style from './assets/css/reset.css'

export default {
	name: 'app',
	components: {
		mainGnb,
		mainSlide,
		mainSolution,
		mainproject,
		mainFooter,
		mainNews,
		mainclients
	}
}
</script>

<style>
.appInner {
	/* max-width: 1920px;
	margin:0 auto 100px; */
	padding:0 2.5vw
}
</style>
