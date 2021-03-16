<template>
	<div>
		<div v-for="Content in Contents">
			<concrete-desc :Content="Content"></concrete-desc>
		</div>
	</div>
</template>

<script>
import ConcreteDesc from "@/components/common/ConcreteDesc";
export default {
	props: [],
	components: {
		ConcreteDesc
	},
	watch: {},
	data() {
		return {
			Contents: [
				{
					imgUrl:[
						require('../../../static/CourseDesigns/DIP_Example1.png'),
						require('../../../static/CourseDesigns/DIP_Example2.png'),
						require('../../../static/CourseDesigns/DIP_Compare.png'),
					],
					name: "Sky Replacement based on U-Net--Course Design of Digital Image Processing",
					members:[
						"Jing Wu",
						"Yuan Liu",
						"Zhao Shen",
					],
					instructor:"Jia Yan, WuHan University",
					instructorUrl:"http://eis.whu.edu.cn/ryDetail.shtml?rsh=00009887",
					intro:"Sky is a common background in photos, but because of the limited time of photographing, " +
						"it is usually not very interesting. In this project, we proposed an automatic background replacement " +
						"algorithm that can generate realistic, artifact-free images with a diverse styles of skies. " +
						"The key idea of our algorithm is to use semantic segmentation to guide the entire process, " +
						"including sky segmentation, replacement, color transfer and guide filter. Plus, we implement our algorithm " +
						"into video process. Even if it can’t be played real time, the outcome still performs well.",
					result:"",
					demoUrl:"../../../static/CourseDesigns/DIP_Demo.mp4",
					projectUrl:"../../../static/CourseDesigns/Report_SkyReplacement.pdf",
				},
			],
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

<style lang='' scoped>

</style>