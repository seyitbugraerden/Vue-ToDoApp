<template>
  <div id="app">
    <InputArea/>
    <CardArea/>
  </div>
</template>

<script>
import CardArea from './components/CardArea.vue';
import InputArea from './components/InputArea.vue';
export default {
  data(){
    return{
    }
  },
  components : {
    CardArea,
    InputArea
  },
}
</script>
