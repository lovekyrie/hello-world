<template>
  <div class="input-wrap">
    <h3>TODO LIST</h3>
    <input type="text" v-model="todoContent" @keyup.enter="submit" />
  </div>
</template>
<script>
import { ref } from "vue";
export default {
  setup(props, context) {
    const todoContent = ref("");
    const submit = () => {
      context.emit("submit", todoContent);
    };
    return { todoContent, submit };
  },
};
</script>
<style lang="less" scoped>
.input-wrap {
  text-align: center;
  h3 {
    text-align: center;
  }
  input {
    border: 2px solid #333;
    width: 90vw;
    padding: 5px 10px;
    font-size: 24px;
  }
}
</style>
