<template class>
   <div class="bg-danger-subtle p-3">
      <div class="bg-dark text-light text-center p-3 mb-3">
        <h1>MY TO DO LIST</h1>
    </div>
    <div>
      <addtask @add-task="addNewTask"/>
      
    </div>
    <br>
    <div>
        <listtask :task="task"/>
    </div>
   </div>
  
</template>
<script>
import addtask from '@/components/addtask.vue'
import listtask from '@/components/listtask.vue'
export default {
    components:{
        addtask,
        listtask  
    },
    data(){
        return{
            task:[]
        }
    },
    methods:{
        addNewTask(newTask){
            this.task.push({title: newTask,checked:false})
            console.log(this.task)
        }
    }
}

</script>

<style >

</style>
