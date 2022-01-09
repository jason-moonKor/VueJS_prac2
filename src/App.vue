<template>
	<div>
		<!-- <h1>{{ count }}</h1>
		<button @click="addNum">숫자 증가</button>
		<button @click="miNum">숫자 감소</button>
		<button @mouseover="addNum2(10)">마우스오버</button> -->
		<h2>{{ msg }}</h2>
		<!-- <button @click="greeting">인사</button>
		<button @click="goodBye">작별</button> -->
		<!-- <div @click="MousePosition" class="box"></div> -->
		<button @click="addNum3($event, 10)">10더하기</button>
		<button @click="addNum3($event, 100)">100더하기</button>
	</div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			count: 0,
			msg: ""
		};
	},
	methods: {
		MousePosition(e) {
			console.log(e);
			this.msg = `마우스의 위치는 ${e.pageX},${e.pageY}`;
		},
		greeting() {
			this.msg = "안녕하세요";
		},
		goodBye() {
			this.msg = "잘가";
		},
		addNum() {
			this.count++;
		},
		addNum2(a) {
			this.count = this.count + a;
		},
		addNum3(e, v) {
			this.msg = `마우스좌표 ${e.pageX}와 + ${v} = ${e.pageX + v}입니다`;
		},
		miNum() {
			this.count--;
			if (this.count < 0) {
				this.count = 0;
			}
		}
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
button {
	width: 200px;
	height: 100px;
	font-size: 24px;
}
.box {
	width: 300px;
	height: 300px;
	background-color: orange;
}
</style>
