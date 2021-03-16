<template>
    <div class="bgColor">
	    <div class="navigator">
			<navigator-mgr></navigator-mgr>
	    </div>
	    <div class="itemContent">
			<div class="leftArea">
				<tabs-table :tab-items="menu" :isActive="isActive" v-on:clickEvent="changeIsActive">
					<div class="scrollArea">
						<div class="itemContent" v-if="isActive===menu[0].value">
							<curriculum-vitae></curriculum-vitae>
						</div>
						<div class="itemContent" v-if="isActive===menu[1].value">
							<research-mgr></research-mgr>
						</div>
						<div class="itemContent" v-if="isActive===menu[2].value">
							<design-mgr></design-mgr>
						</div>
						<div class="itemContent" v-if="isActive===menu[3].value">
							<activity-mgr></activity-mgr>
						</div>
						<div class="itemContent" v-if="isActive===menu[4].value">
							To be updated...
						</div>
					</div>
				</tabs-table>

			</div>
			<div class="rightArea">
				<personal-info></personal-info>
		    </div>
	    </div>
    </div>
</template>

<script>
	import PersonalInfo from "@/components/PersonalInfo";
	import NavigatorMgr from "@/components/NavigatorMgr";
	import TabsTable from "@/components/TabsTable";
	import CurriculumVitae from "@/components/CV/CurriculumVitae";
	import ResearchMgr from "@/components/Researches/ResearchMgr";
	import DesignMgr from "@/components/CourseDesigns/DesignMgr";
	import ActivityMgr from "@/components/SocialActivities/ActivityMgr";
    export default {
    	name: "MainPage",
        props: [],
	    components: {
	        PersonalInfo,
		    NavigatorMgr,
		    TabsTable,
		    CurriculumVitae,
		    ResearchMgr,
		    DesignMgr,
		    ActivityMgr,
	    },
	    watch: {},
        data() {
            return {
                isActive:"1",
	            menu:[
	            	{
	            		name: "Curriculum Vitae",
			            value: "1",
			            comp: "",
		            },
		            {
			            name: "Research & Project",
			            value: "2",
			            comp: "",
		            },
		            {
			            name: "Course Design",
			            value: "3",
			            comp: "",
		            },
		            {
			            name: "Social Activity",
			            value: "4",
			            comp: "",
		            },
		            {
			            name: "Life & Hobbies",
			            value: "5",
			            comp: "",
		            },
	            ],
            }
        },
        created() {
        },
        mounted() {
        },
        methods: {
    		changeIsActive(value){
    			this.isActive = value;
		    }
        },
        beforeDestroy() {
        }
    }
</script>

<style scoped>
	.navigator{
		width: 100%;
		height: 200px;
		border-radius: 50px;
	}

	.rightArea{
		float: right;
		width: 300px;
		height: 700px;
		overflow: hidden;
	}

	.leftArea{
		height: 100%;
		float: left;
		width: calc(100% - 300px);
		/*background-color: #42b983;*/
	}

	.bgColor{
		background-color: #77798f;
	}

	.itemContent{
		width: 100%;
		height: 100%;
		/*background-color: bisque;*/
	}

	.scrollArea{
		height: 100%;
		overflow-y: visible;
		overflow-x: hidden;
	}
</style>
