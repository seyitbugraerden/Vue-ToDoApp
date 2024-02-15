<template>
    <div id="app">
        <Card>
            <template #title>Görevler</template>
            <template #content>
                <InputArea @enteredValue="enteredNewValue = $event" />
                <p>{{ enteredNewValue }}</p>
            </template>
        </Card>
    </div>
</template>

<script>
import Card from 'primevue/card';
import InputArea from './InputArea.vue';

export default {
    components: {
        Card,
        InputArea
    },
    data() {
        return {
            enteredNewValue: ''
        };
    }
}
</script>
