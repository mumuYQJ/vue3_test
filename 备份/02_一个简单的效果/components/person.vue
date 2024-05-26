<template>
  <div>
    <p>{{ name }}</p>
    <button @click="showAge">查看年龄</button>
    <button @click="showSex">查看性别</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "person",
  data() {
    return {
      name: "张三",
      age: 18,
      sex: "男",
    };
  },
  methods: {
    showAge() {
      this.age++;
      alert(this.age);
    },
    showSex() {
      alert(this.sex);
    },
  },
});
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
