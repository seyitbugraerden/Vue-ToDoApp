<template>
  <div id="app">
    <CardArea :title="titleData"/>
  </div>
</template>

<script>
import CardArea from './components/CardArea.vue';
export default {
  data(){
    return{
      titleData : 'Gönderilen Veri'
    }
  },
  components : {
    CardArea
  },
}
</script>
