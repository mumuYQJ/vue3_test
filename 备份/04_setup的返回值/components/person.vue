<template>
  <div>
    <p>{{ name }}</p>
    <p>{{ age }}</p>
    <p>{{ sex }}</p>
    <button @click="showAge">查看年龄</button>
    <button @click="showSex">查看性别</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "person",
  setup() {
    let name = "李四";
    let age = 18;
    let sex = "女";

    function showAge() {
      age++;
      alert(age);
    }

    function showSex() {
      alert(sex);
    }

    return () => "哈哈";
    // return function () {
    //   return "嘿嘿";
    // };
  },
});
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
