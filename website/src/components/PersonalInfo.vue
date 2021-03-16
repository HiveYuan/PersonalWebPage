<template>
    <div class="sideArea" id="PersonalInfo">
	    <img class="photo" src="../assets/lifephoto.jpg" alt="">
	    <div class="fonts">WuHan University</div>
	    <div class="fonts">E-mail: hiveyuan@gmail.com</div>
	    <div class="compoCenter">
		    <a class="linkFont" href="https://github.com/HiveYuan">My github: HiveYuan</a>
	    </div>
    </div>
</template>

<script>
	export default {
        name: "PersonalInfo",
        props: [],
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
	    components: {},
	    beforeDestroy() {
	    }
	  }
</script>

<style scoped>
	.photo{
		width: 100%;
		border-radius: 50px;
		height: auto;
	}

	.sideArea{
		border-radius: 50px;
		float: right;
		width: 300px;
		height: 100%;
		background-color: #c0c6c6;
	}

	.fonts{
		font-family: Georgia ;
		font-size: 16px;
		text-align: center;
		font-style:italic;
		margin: 5px;
	}
	.linkFont{
		width: 100%;
		font-family: Georgia ;
		text-align: center;
		text-decoration: none;
		color: #2368f9;
		font-style:italic;
		font-size: 16px;
		margin: 0 auto;
		margin: 5px;
	}

	.linkFont:hover{
		color: #00ffff;
	}

	.compoCenter{
		text-align: center;
	}
</style>
