<template>
    <div id="app">
        <Card>
            <template #title>Görevler</template>
            <template #content>
                <div class="InputArea"><InputArea @enteredValue="addTask" /></div>
                <div class="taskArae">
                    <div class="task" v-for="task in taskList" :key="task.id"><span :title="task.text">{{ task.text }}</span> <button @click="deleteTask(task.id)">Delete</button></div>   
                </div>
            </template>
        </Card>
    </div>
</template>

<script>
import { nanoid } from 'nanoid';
import Card from 'primevue/card';
import InputArea from './InputArea.vue';

export default {
    components: {
        Card,
        InputArea
    },
    data() {
        return {
            taskList : []
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
