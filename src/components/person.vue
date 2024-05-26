<template>
  <div>
    <p>{{ name }}</p>
    <p>{{ age }}</p>
    <p>{{ sex }}</p>
    <button @click="showAge">查看年龄</button>
    <button @click="showSex">查看性别</button>
    <button @click="a">a</button>
    <button @click="b">b</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "person",

  data() {
    return {
      name: "王武",
      age: 20,
      sex: "男",
    };
  },

  methods: {
    a() {
      alert("a");
    },
    b() {
      alert("b");
    },
  },

  setup() {
    let name = "赵六";
    let age = 18;
    let sex = "女";

    function showAge() {
      age++;
      alert(age);
    }

    function showSex() {
      alert(sex);
    }

    // return () => "哈哈";
    // return function () {
    //   return "嘿嘿";
    // };

    return { name, age, sex, showAge, showSex };
  },
});
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
