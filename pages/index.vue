<template>
    <div class="todo__wraper">
        <!---<h2>Manage all youe task at a sigle place</h2>-->
        <div class="todo__task-list">

            <div class="todo_add">
                <button class="btn" @click="toogleDialog">Adicionar Nova Tarefa</button>

            </div>
            <h3>Tarefa Ativa</h3>
            <!--- the active task list -->
            <div v-for="(item, index) in [1,2,3,4]" :key= index>
                <TaskCard/>
            </div>

            <h3>Tarefa Concluída</h3>
            <!--- the active task list -->
            <div v-for="(item, index) in [1,2,3,4]" :key= index>
                <TaskCard/>
            </div>
            
        </div>
        <AddTask v-if="showDialog" @close="toogleDialog"></AddTask>
    </div>
 </template> 
 <style scoped>


</style>  

<script setup lang="ts">
import AddTask from '~/component/AddTask.vue';
import TaskCard from '~/component/TaskCard.vue';

import {ref} from "vue";
const showDialog= ref(false);

function toogleDialog(){
    showDialog.value= !showDialog.value;
}
</script>