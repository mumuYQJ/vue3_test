<template>
  <div>
    <p>姓名：{{ person.name }}</p>
    <p>年龄：{{ person.age }}</p>
    <button @click="changeName">修改姓名</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="changePerson">修改对象</button>
  </div>
</template>

<script lang="ts" setup name="person">
import { ref, watch } from "vue";

let person = ref({
  name: "张三",
  age: 18,
});

function changeName() {
  person.value.name += "~";
}

function changeAge() {
  person.value.age++;
}

function changePerson() {
  person.value = {
    name: "李四",
    age: 17,
  };
}

watch(
  person,
  (newValue, oldValue) => {
    console.log("person对象修改", newValue, oldValue);
  },
  { deep: true, immediate: true }
);
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
