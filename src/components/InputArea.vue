<template>
    <div>
        <InputText v-model="value" @keypress.enter="AddTask" placeholder="Add Your Task"/>
        <Button label="Add" @click="AddTask" />
    </div>
</template>

<script>
import InputText from 'primevue/inputtext';
import Button from 'primevue/button';

export default {
    data() {
        return {
            value: ''
        }
    },
    components: {
        InputText,
        Button
    },
    methods: {
        AddTask() {
            console.log(this.value);
            if(this.value != ''){
            this.$emit("enteredValue", this.value)}
            this.value = ''
        }
    }
}
</script>
