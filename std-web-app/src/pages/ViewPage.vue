<template>
	<div>
		<div id="task-list">
			<h1> Current Tasks to handle </h1>
		</div>
		<input class="newTodo" autofocus autocomplete="off" placeholder="Enter a new task here" v-model="newTask" v-bind:key="this.isChanged"/>
		<button @click="addTask(newTask);">Enter </button>
		<ul>
			<div v-bind:key="this.isChanged">
				<li v-for="(item,index) in tasks" v-bind:key=item.index> <!-- must bind -->
					<task v-bind:expression="item" />
					<button class="delete-button" @click="deleteTask(index)"><strong>X</strong></button>
				</li>
			</div>
		</ul>
	</div>
</template>

<script>
import task from '../components/task.vue'

export default {
	name: "ViewPage",
	components:{
		task,
	},
	data(){
		return{
			tasks: ['first','second','third','fourth'],
			isChanged:0,
		}
	},
	methods:{
		deleteTask: function(value){
			this.tasks.splice(Number(value),1)
			this.isChanged++
		},
		addTask: function(value){
			alert(value)
			this.tasks.unshift(value)
			this.isChanged++	
			value=""
		}
	}

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

li{
	list-style:none;
}

ul{
	width:450px;
	margin-left:auto;
	margin-right:auto;
}

#task-list{
	text-align:center;
}

.delete-button{
	background-color:transparent;
	border:none;
	color:black;
	text-align:center;
	width:20px;
	height:20px;
	position:relative;
	bottom:25px;
	left:180px;
	outline: none !important;
	outline-offset: none !important;
	margin-left:180px;
}

</style>
