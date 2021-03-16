<template>
	<div>
		<div class="tittle">RESEARCHES</div>
		<div class="listArea">
			<div class="cont" v-for="item in researchItems">
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
	name: "ResearchPart",
	props: [],
	watch: {},
	data() {
		return {
			researchItems:[
				{
					value:"1",
					name: "3D Scene Rendering Based on Photon Mapping",
					time: "07/2020-09/2020",
					information: "Accelerated Algorithm Research, Guided by Prof. James O’Brien, University of California, Berkeley",
					intro:"-The project aimed to optimize the previous renderers based on computer graphics and photon mapping and find a " +
						"rendering algorithm that consumes less time.",
					myJob:"-My job was to optimize the data structure and process multithreading and finally, we successfully reduced the rendering " +
						"time from 3034.22 seconds to 2504. 25 seconds for a complex 3D scene.",
				},
				{
					value:"2",
					name: "Intelligent Robotic Arm Control System Based on Computer Vision",
					time: "03/2019-03/2020",
					information: "Research Member of Robotic Arm Drive, Digital Signal Processing Lab, EIS, WHU",
					intro:"-Researched on robot modeling and control based on Robot Operating System.",
					myJob:"-Responsible for correcting the possible accuracy problem of eye-in-hand calibration and the problem of inaccurate poseduring " +
						"target recognition, and transplanted all the researched platforms to JETSON TX2",
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