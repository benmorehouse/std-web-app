<template>
	<div class="task-body-background">
		<div class="task-body">
			<div class="task-text">
				{{expression}}
			</div>
		</div>
	</div>
</template>

<script>

export default {
	name: "task",
	props:{
		expression: String,
	},
}

</script>

<style>
.task-text{
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	text-align:center;
	font-size:15px;
	color:black;
	padding:5px;
}

.task-body{
	position:relative;
	left:1px;
	top:1px;
	background-color:#ffd700;
	border-radius:10px;
	height:30px;
	width:400px;
}

.task-body-background{
	background-color:black;
	border-radius:10px;
	height:32px;
	width:402px;
}

</style>
