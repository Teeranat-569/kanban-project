<template>
  <div id="app">
    <KanBan />
  </div>
</template>

<script>
import KanBan from "./components/KanBan.vue";

export default {
  name: "App",
  components: {
    KanBan,
  },
};
</script>

<style>
#app {

  height: 100vh;
}
</style>
