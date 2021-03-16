<template>
	<div>
		<a class="linkFont" href="../../../static/CV/CV_Hive(Yuan%20Liu).pdf">CV_Hive(YuanLiu).pdf_Download</a>
		<div class="areaWrapper">
			<education-part></education-part>
		</div>
		<div class="areaWrapper">
			<research-part></research-part>
		</div>
		<div class="areaWrapper">
			<internship-part></internship-part>
		</div>
		<div class="areaWrapper">
			<important-course-design></important-course-design>
		</div>
		<div class="areaWrapper">
			<social-activity></social-activity>
		</div>
	</div>
</template>

<script>
import EducationPart from "@/components/CV/EducationPart";
import ResearchPart from "@/components/CV/ResearchPart";
import InternshipPart from "@/components/CV/InternShipPart";
import ImportantCourseDesign from "@/components/CV/ImportantCourseDesign";
import SocialActivity from "@/components/CV/SocialActivity";
export default {
	name: "CurriculumVitae",
	props: [],
	components: {
		EducationPart,
		ResearchPart,
		InternshipPart,
		ImportantCourseDesign,
		SocialActivity
	},
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
	.areaWrapper{
		margin-bottom: 20px;
	}

	.linkFont{
		width: fit-content;
		font-family: "Times New Roman" ;
		text-align: right;
		text-decoration: none;
		color: #2368f9;
		font-size: 18px;
		margin: 0 auto;
		margin: 5px;
		float: right;
	}

	.linkFont:hover{
		color: #00ffff;
	}
</style>