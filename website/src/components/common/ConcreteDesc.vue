<template>
	<fieldset class="descArea">
		<div class="tittle">{{Content.name}}</div>
		<div class="imgArea">
			<img v-for="imgUrl in Content.imgUrl" class="imgStyle" :src="imgUrl" alt="Failed to load the image!">
		</div>
		<div class="contentArea">
			<div class="Area">
				<div class="subTittle">Team:</div>
				<div class="widthFit" v-for="member in Content.members">{{member}},&nbsp;&nbsp;&nbsp;</div>
			</div>
			<br>
			<div class="Area">
				<div class="subTittle">Instructor:</div>
				<a class="linkFont" :href="Content.instructorUrl">
					{{Content.instructor}}</a>
			</div>
			<br>
			<div class="Area" v-if="Content.intro">
				<div class="subTittle">Introduction:</div>
				<div class="widthFit" style="width:90%;">{{Content.intro}}</div>
			</div>
			<br>
			<div class="Area" v-if="Content.result">
				<div class="subTittle">Results:</div>
				<div class="widthFit" style="width:90%;">{{Content.result}}</div>
			</div>
			<br>
			<div class="Area" v-if="Content.demoUrl">
				<div class="subTittle">Demo:</div>
				<video :src="Content.demoUrl" width="80%" height="auto" controls="controls">
				</video>
				<div class="widthFit" style="font-family: 'Microsoft YaHei UI Light';font-size: 16px;font-weight: bold">
					Note : To play the video, Chrome 5.0+ is recommended.
				</div>
			</div>
			<div class="Area" v-if="Content.projectUrl" style="font-weight: bold;">
				<div class="widthFit">
					For more details about our project, please&nbsp;
				</div>
				<a class="linkFont" :href="Content.projectUrl">
					click here</a>
			</div>
		</div>
	</fieldset>
</template>

<script>
export default {
	props: [
		"Content",
	],
	components: {},
	watch: {},
	data() {
		return {
			name: "",
		}
	},
	created() {
	},
	mounted() {
	},
	methods: {},
	beforeDestroy() {
	}

}
</script>

<style scoped>
	.contentArea{
		width: 60%;
		height: auto;
		/*background-color: #dbd565;*/
		float: right;
		border-radius: 50px;
	}

	.imgStyle{
		width: 100%;
		/*width: 520px;*/
		height: auto;
		/*border-radius: 50px;*/
	}

	.descArea{
		margin: 10px;
		height: 100%;
		width: calc(100% - 50px);
		border-radius: 50px;
		border: 2px solid #3f4845;
		float: left;
	}

	.tittle{
		width: 100%;
		font-family: "Times New Roman";
		font-weight: bold;
		font-size: 30px;
		padding-bottom: 3px;
		margin: 5px;
		text-align: center;
	}

	.Area{
		width: calc(100% - 50px);
		float: left;
		font-family: "Times New Roman";
		border-radius: 50px;
		font-size: 20px;
		padding-bottom: 3px;
		margin-left: 50px;
		margin-top: 10px;
		margin-bottom: 10px;
	}

	.widthFit{
		width: fit-content;
		float: left;
		text-align:justify;
		text-justify: distribute-all-lines;
		line-height: 26px;
	}

	.subTittle{
		width: fit-content;
		font-size: 26px;
		font-weight: bold;
		margin-bottom: 10px;
	}

	.linkFont{
		width: fit-content;
		font-family: "Times New Roman" ;
		text-decoration: none;
		color: #185ff0;
		font-size: 20px;
		float: left;
		line-height: 26px;
	}

	.linkFont:hover{
		color: #00ffff;
	}

	.imgArea{
		width: 40%;
		height: auto;
		border-radius: 50px;
		float: left;
	}
</style>