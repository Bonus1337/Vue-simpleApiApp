<template>
  <GetList />
  <PostList />
</template>

<script>
import PostList from "./components/PostList.vue";
import GetList from "./components/GetList.vue";
export default {
  name: "App",
  components: {
    GetList,
    PostList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
