<template>
    <div id="app">
        <Card>
            <template #title>Taskes</template>
            <template #content>
                <div class="InputArea"><InputArea @enteredValue="addTask" /></div>
                <div class="taskArae">
                    <div class="task" v-for="task in taskList" :key="task.id"><span :title="task.text">{{ task.text }}</span> <button @click="deleteTask(task.id)">Completed</button></div>   
                </div>
            </template>
        </Card>
    </div>
</template>

<script>
import { nanoid } from 'nanoid';
import Card from 'primevue/card';
import InputArea from './InputArea.vue';
import data from '../data/db.json'

export default {
    components: {
        Card,
        InputArea
    },
    data() {
        return {
            taskList : data
        };
    },
    methods : {
        addTask(taskText){
            const task = {
                id: nanoid(),
                text: taskText
            };
            this.taskList.push(task);
        },
        deleteTask(taskId) {
        this.taskList = this.taskList.filter(task => task.id !== taskId);
    }
    }
}
</script>
<style>
.task {
    display: flex;
    justify-content: space-between;
    margin: 10px 0px;
    align-items: center;
}

.task button {
    transform: scale(0.8);
    transform-origin: right;
}

.task:nth-child(even) {
    background-color: rgba(162, 168, 211, 0.1);
}

.task span {
    max-width: 200px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.InputArea {
    margin-bottom: 50px;
}


</style>