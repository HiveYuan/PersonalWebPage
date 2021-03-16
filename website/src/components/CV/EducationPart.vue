<template>
	<div>
		<div class="tittle">EDUCATION</div>
		<div class="subTittle">
			<div class="left">WuHan University(WHU), WuHan, China</div>
			<div class="right">09/2017-06/2021</div>
		</div>
		<ul class="listArea">
			<li class="cont" v-for="item in listItem">
				{{item.content}}
			</li>
		</ul>
		<div class="awards">
			<div class="leftAlign">-Extraordinary Student Leader in WHU</div>
			<div class="right">04/2020</div>
		</div>
		<br>
		<div class="awards">
			<div class="leftAlign">-Third Tier Merit Scholarship based on GPA performance among top 30%</div>
			<div class="right">10/2019</div>
		</div>
		<br>
		<div class="awards">
			<div class="leftAlign">-Elite Student of WHU based on integrated campus performance among top 30%</div>
			<div class="right">10/2019</div>
		</div>
		<br>
		<div class="awards">
			<div class="leftAlign">-Outstanding Student Leader in Student Council of WHU among top 10%</div>
			<div class="right">05/2019</div>
		</div>
		<br>
	</div>
</template>

<script>
export default {
	name: "EducationPart",
	props: [],
	watch: {},
	data() {
		return {
			listItem:[
				{
					value:"1",
					content:"BS in Electronic Information Engineering, Electronic Information School (EIS)",
				},
				{
					value:"2",
					content:"GPA: 3.58/4.0, GRE 323 (V153+Q170+W3.5), TOEFL: 102 (28+24+25+25)",
				},
				{
					value:"3",
					content:"Program Language: C++, Python, Java, JavaScript, HTML, VUE",
				},
				{
					value:"4",
					content:"Software: Visual Studio 2015, IDEA, PyCharm, VS Code",
				},
				{
					value:"5",
					content:"Systems: Win10, Linux (Ubuntu)",
				},
				{
					value:"6",
					content:"Academic Honors & Leadership Awards:",
				},
			]
		}
	},
	created() {
	},
	mounted() {
	},
	methods: {},
	components: {},
	beforeDestroy() {
	}

}
</script>

<style scoped>
	.tittle{
		width: fit-content;
		font-family: "Times New Roman";
		font-weight: bold;
		font-size: 30px;
		border-bottom: 2px solid black;
		padding-bottom: 3px;
		margin: 5px;
	}

	.subTittle{
		width: 100%;
		height: 22px;
		font-family: "Times New Roman";
		font-weight: bold;
		font-size: 22px;
		padding-bottom: 3px;
		margin: 5px;
	}

	.cont{
		font-family: "Times New Roman";
		font-size: 20px;
		margin: 5px;
	}

	.left{
		float: left;
	}

	.leftAlign{
		float: left;
		margin-left: 45px;
	}

	.right{
		float: right;
		margin-right: 15px;
	}

	.awards{
		width: 100%;
		font-family: "Times New Roman";
		font-size: 20px;
		margin: 5px;
	}

	.listArea{
		margin: 5px;
	}
</style>