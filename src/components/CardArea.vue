<template>
    <div id="app">
        <Card>
        <InputArea @enteredValue="receiveEnteredValue"/>
            <template #title>Görevler</template>
            <template #content>
                <InputArea/>
            </template>
        </Card>
    </div>
</template>

<script>
import Card from 'primevue/card';
import InputArea from './InputArea.vue';

export default {
    el: '#app', 
    data(){
        return{

        }
    },
    components: {
        Card,
        InputArea
    },

    data() {
        return {
          receiveEnteredValue : ''  
        };
    },
}
</script>
