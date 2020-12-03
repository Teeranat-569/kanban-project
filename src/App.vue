<template>
  <div id="app">
    <KanBan :data="data" />
  </div>
</template>

<script>
import KanBan from "./components/KanBan.vue";

export default {
  name: "App",
  components: {
    KanBan,
  },
  data(){
    return {
      data:[
        {
          name :"todo",
          color:"#F4B58E",
          tasks:[]
        },
        {
          name :"doing",
          color:"#F363B1",
          tasks:[]
        },
        {
          name :"done",
          color:"#FF9420",
          tasks:[]
        }
      ]
    }
  }
};
</script>

<style>
#app {

  height: 100vh;
}
</style>
