<template>
  <div id="app">
    <KanBan :data="data" :create_task_submit="create_task_submit"/>
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
          tasks:[
            {task_name: "test"}
          ]
        },
        {
          name :"doing",
          color:"#F363B1",
          tasks:[ {task_name: "test"}]
        },
        {
          name :"done",
          color:"#FF9420",
          tasks:[ {task_name: "test"}]
        }
      ]
    }
  },
  methods:{
    create_task_submit(column_index,item){
      this.data[column_index].tasks.push(item)
    }
  }
};
</script>

<style>
#app {

  height: 100vh;
}
</style>
