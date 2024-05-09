<template>
    <div>
        <h3 class="mb-3">Add Task</h3>
        <form @submit.prevent="addTask" class="row g-2">
        <div class="col">    
             <input type="text" v-model="newTask" class="form-control" placeholder="add task"> 
        </div>
        <div class="col-auto">
            <button class=" btn btn-success ml-2 " type="submit">add</button>
        </div>
        </form>
    </div>
</template>
<script >
export default {

    data(){
        return{
            newTask:"",
        }
    },
    methods:{
        addTask(){
            if(this.newTask.trim() !== "") {
                
                this.$emit('add-task', this.newTask)
                this.newTask = ""
            }
        }
    }
}

</script>

<style scoped>

</style>
