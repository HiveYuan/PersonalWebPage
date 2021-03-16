<template>
	<div>
		<div class="tittle">LEADERSHIP & VOLUNTARY INVOLVEMENTS</div>
		<div class="listArea">
			<div class="cont" v-for="item in activityItems">
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
	name: "SocialActivity",
	props: [],
	watch: {},
	data() {
		return {
			activityItems:[
				{
					value:"1",
					name: "The 9th&10th Youth Leader Communication Summit between Mainland and Hong Kong & Macau",
					time: "04/2019&2018",
					information: "",
					intro:"-Invited a total of 90 youth representatives from about 30 universities across the country " +
						"to Wuhan University to participate in the 7-day summit discussions as the Summit President.",
					myJob:"-Responsible for the whole event planning, personnel arrangement, material coordination and " +
						"guest reception, and managed overall plans and made major decisions.",
				},
				{
					value:"2",
					name: "President of Youth League of the EIS, WU",
					time: "09/2018-01/2019",
					information: "",
					intro:"",
					myJob:"-Organized routine activities to enrich our campus life like festival carnivals for celebrating " +
						"traditional festivals or special days like international labors’ day etc.",
				},
				{
					value:"3",
					name: "Voluntary Teacher,\"Sunny Home Tutor One-on-One Project\"",
					time: "12/2017",
					information: "",
					intro:"",
					myJob:"-Tutored the primary school students in the “Sunny Home” Child Center in the Ziyang Street, " +
						"Wuchang District, Wuhan City, and melt in them to play games etc.",
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