<template>
	<div>
		<div class="menuWrapper">
			<div v-for="item in tabItems"
			     :class="isActive===item.value? 'itemStyleClicked':'itemStyle'"
			     @click="itemClick(item.value)">
				{{item.name}}
			</div>
		</div>
		<div class="itemContent">
			<slot></slot>
		</div>
	</div>
</template>

<script>
export default {
	name: "TabsTable",
	props: [
		"tabItems",
		"isActive",
	],
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
	methods: {
		itemClick(value){
			this.$emit("clickEvent",value);
		}
	},
	components: {},
	beforeDestroy() {
	}

}
</script>

<style scoped>
	.menuWrapper{
		width: 100%;
		height: 40px;
		border-bottom: 2px solid #2c3e50;
	}

	.itemStyle {
		list-style: none;
		float: left;
		font-family: "Microsoft YaHei UI";
		margin-left: 20px;
		font-size: 26px;
		border-radius: 5px;
		padding: 3px;
	}
	.itemStyleClicked {
		list-style: none;
		float: left;
		font-family: "Microsoft YaHei UI";
		margin-left: 20px;
		font-size: 26px;
		border-radius: 5px;
		padding: 3px;
		background-color: red;
	}

	.itemStyleClicked:hover {
		cursor: pointer;
	}

	.itemStyle:hover{
		cursor: pointer;
		background-color: #cf5a5a;
	}

	.itemContent{
		width: 100%;
		height: 100%;
		/*background-color: bisque;*/
	}

</style>