<template>
    <div >
    <h3 class="mx-3">ALL TASK</h3>
        <ul v-for="(task, index) in task" :key="index" class="">
            <li class="border border-secondary p-3 rounded-2">
                <p class="text-25" :class="{ 'text-decoration-line-through': task.checked }"><span class="fs-20 fw-bold text-success tex-uppercase">Task :</span> {{ task.title }}</p>
                <div class="d-flex justify-content-between">
                    <button class="btn btn-danger" @click="deleteTask(index)">Delete</button>
                    <button class="btn btn-success"@click="endTask(index)">Completed</button>  
                </div>
            </li>
        </ul>
    </div>
</template>
<script >
export default {
    props:['task'],
    methods:{
        deleteTask(index){
            this.task.splice(index,1)
        },
        endTask(index){
            console.log(this.task[index].checked)     
            this.task[index].checked =true
            console.log(this.task[index].checked)
        }
        
    }
        
       
       
}

</script>

<style >

 ul{
    list-style-type: none;
 }
 

</style>
