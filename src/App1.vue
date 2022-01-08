<template>
	<div>
		<h1>하이 {{ animal }}</h1>
		<h2>원숭이는 {{ food }} 를 좋아합니다</h2>
		<input type="text" v-model="food" />
		<div v-html="alertMsg"></div>
		<div v-html="subHtml"></div>
		<img :src="imgSrc" alt="random" />
		<br />
		<a :href="food">{{ food }}</a>
		<hr />
		<h2 :class="{red: food === 'apple', 'not-good': food === `rice`}">
			원숭이는 {{ food }} 를 좋아합니다
		</h2>
		<h2>원숭이는 {{ food }} 를 좋아합니다</h2>
	</div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			animal: "monkey",
			food: "apple",
			alertMsg: "<h2>경고</h2>",
			subHtml: `<button onclick="document.querySelector('body').style.backgroundColor = 'beige'">클릭</button>`,
			imgSrc: "http://placeimg.com/700/300/any",
			naverUrl: "https://www.naver.com"
		};
	}
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
input {
	font-size: 20px;
}
.orange {
	color: orange;
}
.salmon {
	color: salmon;
}
.red {
	color: red;
}
.not-good {
	text-decoration: line-through;
}
</style>
