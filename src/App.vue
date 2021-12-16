<template>
  <Inputer @submit="subSubmit"></Inputer>
  <div v-for="(todo, index) in list" :key="index">{{ todo }}</div>
</template>

<script>
import Inputer from "./components/Inputer.vue";
export default {
  name: "App",
  components: {
    Inputer,
  },
  data() {
    return {
      list: [],
    };
  },
  methods: {
    subSubmit(e) {
      this.list.push(e);
    },
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
