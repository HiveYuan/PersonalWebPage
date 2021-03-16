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
					imgUrl:[require('../../../static/Researches/CG_REPORT.png')],
					name: "3D Scene Rendering Based on Photon Mapping",
					members:[
						"Ellen(Yi Ge)",
						"Hive(Yuan Liu)",
						"Raymond(Rui Wang)",
						"Mia(Xiaoyu Liu)",
						"Chenhan Lyu",
					],
					instructor:"James F. O'Brien, University of California,Berkeley",
					instructorUrl:"http://obrien.berkeley.edu/Prof._James_F._OBrien/Home.html",
					intro:"Since ray-tracer occurs to have some disadvantages when dealing with indirect " +
						"illuminations such as bleeding and caustics, we would like to apply photon mapping to " +
						"achieve more complicated rendering. Photon mapping is a two-pass global illumination " +
						"rendering algorithm that approximately solves the rendering equation for integrating " +
						"light radiance at a given point in space. Our project includes two parts: K-D Tree and " +
						"Shading. As for the first section, two K-D trees will be used. One for storing the " +
						"bounding box of photons. The other for storing the bounding box of objects. After " +
						"storing the photon and bounding box, we will add the results of photon mapping based " +
						"on the ray-tracer.",
					result:"We used different algorithms to render our models including ray tracing, " +
						"photon mapping and progressive photon mapping for different iterations and" +
						"the time they consume are above. Also, we visualized the photon map to help" +
						"see what role it plays in shading. The figure shows our results. Compared with" +
						"photon mapping, ray tracing shows two drawbacks. Firstly, As is can be seen" +
						"in model 2, surfaces of the red rabbit which cannot be shot hit by the lights" +
						"are completely dark. However, in reality we should still see it because of the" +
						"indirect illumination. Secondly, ray tracing cannot render caustics while photon mapping performs well on it. Our visualization of photon map illustrates" +
						"that photon mapping solve the two shortcomings mentioned above. In PM, we" +
						"also change the number of total photons and the number of sampled photons at" +
						"each hit point. While doing so, we get different outcomes. With only 100,000" +
						"photons in total and 10 ones for each sampling, images are darker than those of" +
						"1,000,000 photons and 500 ones sampled. And because of the insufficiency of" +
						"photons, they show a lot of mottles. In addition, we made a contrast between" +
						"basic photon mapping and progressive photon mapping. For only one iteration," +
						"PPM performs nearly the same as ray tracing. This happens because a very" +
						"limited number of photons were emitted. Thus details were not well shown." +
						"With more photons in the scene, more indirect light rays will be taken into" +
						"account and more details were displayed.",
					demoUrl:"",
					projectUrl:"../../../static/Researches/FinalReport_PhotonMapping_Hive(Yuan%20Liu).pdf",
				},
				{
					imgUrl: [
						require('../../../static/Researches/eye-to-hand.png'),
						require('../../../static/Researches/eye-to-hand.png'),
					],
					name: "Intelligent Robotic Arm Control System Based on Computer Vision",
					members:[
						"Chong Li",
						"Haoren Deng",
						"Tianyi Huang",
						"Yuan Liu",
						"Sijia Liang",
					],
					instructor:"Cien Fan, WuHan University",
					instructorUrl:"http://eis.whu.edu.cn/ryDetail.shtml?rsh=00007285",
					intro:"In this project, we Built a six-degree-freedom robotic arm control system on a " +
						"combination of Jeston TX2, a robotic arm and a RGB-D camera to detect and fetch specific " +
						"items. A CNN based network that combines RGB and RGB-D information is implemented. " +
						"Specifically, we first set up the coordinates systems by eye-to-hand calibration. " +
						"Then an object recognition algorithm based on linemod was used to detect materials. The posture " +
						"and the position of that object were transmitted to the central control system, which would " +
						"afterwards activate the arm to grap the object and put it in the target place.",
					result:"",
					demoUrl:"../../../static/Researches/ArmDemo.mp4",
					projectUrl:"",
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