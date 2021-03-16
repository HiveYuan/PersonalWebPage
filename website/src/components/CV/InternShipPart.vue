<template>
	<div>
		<div class="tittle">INTERNSHIP</div>
		<div class="listArea">
			<div class="cont" v-for="item in internItems">
				<div class="subTittle">
					<div class="left">{{item.name}}</div>
					<div class="right">{{item.time}}</div>
				</div>
				<div class="infoStyle">{{item.information}}</div>
				<div class="content">{{item.intro}}</div>
				<div class="content">{{item.myJob}}</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "InternshipPart",
	props: [],
	watch: {},
	data() {
		return {
			internItems:[
				{
					value:"1",
					name: "Huawei Technologies Co., Ltd. Wuhan Research Institute",
					time: "08/2020-01/2021",
					information: "Software Web Iterative Development Intern, General Development Dep., Wuhan",
					intro:"-Modified the front-end layout architecture of software Web according to customer’s needs and " +
						"improved 10% of the customer satisfaction.",
					myJob:"-Optimized the back-end algorithm, reduced redundant request packets, and shortened the web page " +
						"response time from the original 4s to 1s.",
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

	.right{
		float: right;
		margin-right: 15px;
	}

	.content{
		width: 100%;
		font-family: "Times New Roman";
		font-size: 20px;
		margin: 5px;
	}

	.listArea{
		margin: 5px;
	}

	.infoStyle{
		margin-left: 5px;
		font-family: "Times New Roman" ;
		font-style:italic;
		font-weight: bold;
		font-size: 20px;
	}
</style>