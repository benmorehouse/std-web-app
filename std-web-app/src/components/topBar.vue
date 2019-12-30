<template>

	<div>
		<div class="topBar">
			<h1>STD 2.0 </h1>
			<div class="md-button-wrapper">
				<md-button class="md-raised md-accent" to="/">Main Page</md-button>
				<md-button class="md-raised md-accent" to="/View">View Tasks</md-button>
			</div>
		</div>
		<router-view class="view"></router-view>
		<div class="bottom-bar">
			Copyright 2019 <a href="https://github.com/benmorehouse">Benjamin Morehouse</a>
		</div>
	</div>
</template>

<script>
import Vue from 'vue'
import { MdButton } from 'vue-material/dist/components'
import 'vue-material/dist/vue-material.min.css'
import 'vue-material/dist/theme/default.css'
Vue.use(MdButton)

export default {
	name: "topBar",
}

</script>

<style>

.topBar > h1{
	color:white;
	text-align:center;
	margin-left:auto;
	margin-right:auto;
	margin-top:-10px;
	margin-bottom:-35px;
	padding-top:20px;
	width:150px;
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-text-stroke-width: 1px;
	-webkit-text-stroke-color: black;
}

.topBar{
	margin-left:-10px;
	margin-right:-10px;
	margin-top:-10px;
	margin-bottom:-10px;
	background-color:#c41e3a;
	height:100px;
}


.md-button-wrapper{
	margin-top:40px;
	margin-left:auto;
	margin-right:auto;
	width:430px;
}

.md-button{
	width:200px;
}

.view{
	margin-left:auto;
	margin-right:auto;
	margin-top:10px;
	width:auto;
	border-radius:20px;
	padding:20px;
	min-height:500px;
	background-color:lightgrey;
}

.bottom-bar{
	height:30px;
	margin-left:-10px;
	margin-right:-10px;
	margin-top:20px;
	margin-bottom:0px;
	padding-top:5px;
	font-size:10px;
	color:black;
	text-align:center;
	background-color:#c41e3a;
}

</style>
