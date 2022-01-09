<template>
	<div>
		<!-- <h2>당신의 나이는 {{ age }} 입니다</h2>
		<h3 v-if="age > 18">당신은 성인입니다</h3>
		<h3 v-else-if="13 < age && age <= 18">당신은 청소년 입니다</h3>
		<h3 v-else>당신은 어른이 아닙니다</h3> -->

		<!-- <h2 v-if="display">보입니다</h2>
		<h2 v-show="display">보입니다</h2> -->
		<template v-for="(a, idx) in animals" :key="idx">
			<span v-if="a !== 'monkey'">{{ a }} 인덱스번호: {{ idx }}</span>
			<h2 v-if="a !== 'monkey'"></h2>
		</template>
		<!-- <ul>
			<li v-for="(u, i) in users" :key="i">
				이름은 : {{ u.name }} 직업 : {{ u.job }} 인덱스 번호 = {{ i }}
				<p v-for="i in u.skill" :key="i">{{ i }}</p>
			</li>
		</ul> -->
	</div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			age: 11,
			display: false,
			animals: ["monkey", "rat", "dog", "lion"],
			users: [
				{
					name: "jason",
					job: "developer",
					gender: "male",
					skill: ["html", "javascript", "css"]
				},
				{
					name: "JAY",
					job: "cook",
					gender: "male",
					skill: ["HTML", "JAVA", "JASONSON"]
				},
				{
					name: "FUCK",
					job: "cooker",
					gender: "female",
					skill: ["hhtttmmmll", "javaScript", "cSS"]
				}
			]
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
