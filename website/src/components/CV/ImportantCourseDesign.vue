<template>
	<div>
		<div class="tittle">IMPORTANT COURSE DESIGN</div>
		<div class="listArea">
			<div class="cont" v-for="item in courseItems">
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
	name: "ImportantCourseDesign",
	props: [],
	watch: {},
	data() {
		return {
			courseItems:[
				{
					value:"1",
					name: "Sky Replacement in Image Based on Neural Network",
					time: "04/2020-06/2020",
					information: "Image quality optimization",
					intro:"-Studied the optimization of smooth filtering of image edges and image color style conversion.",
					myJob:"-Optimized the algorithm efficiency and successfully increased the picture switching speed from " +
						"about 7 seconds/frame to 0.65 seconds/frame and the course project won the second place among 11 participating groups.",
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