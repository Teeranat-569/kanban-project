<template>
  <div class="kanban">
    KanBan
    <div
      class="column"
      :style="{ backgroundColor: column.color }"
      v-for="(column, index) in data"
      :key="index"
    >
      <div class="column-header">
        {{ column.name }}
      </div>
      <div class="column-body">
        <div class="create-task" @click="create_task(index)">Create Task</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Array,
  },
  methods:{
      create_task(index_column){
          alert(index_column)
      }
  }
};
</script>

<style>
.kanban {
  width: 100%;
  height: 100%;
  background-color: #564c58;
}
.column {
  height: 600px;
  width: 300px;
  border-radius: 10px;
  display: inline-block;
  margin: 25px;
  -webkit-box-shadow: 7px 10px 20px 0px rgba(199, 199, 199, 1);
  -moz-box-shadow: 7px 10px 20px 0px rgba(199, 199, 199, 1);
  box-shadow: 7px 10px 20px 0px rgba(199, 199, 199, 1);
  padding: 10px;
}
.column-header {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
  font-size: 32px;
  font-weight: bold;
}
.column-body {
  height: calc(100% - 50px);
  background-color: rgba(255, 255, 255, 0.555);
  border-radius: 10px;
  padding: 5px;
}
.create-task {
  width: 100%;
  height: auto;
  padding: 10px;
  border-radius: 5px;
  background-color: black;
  color: white;
  cursor: pointer;
}
.create-task:hover{
    background-color: rgb(255, 255, 255);
    color: black;
}
</style>