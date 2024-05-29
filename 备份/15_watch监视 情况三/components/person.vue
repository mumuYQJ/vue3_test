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
import { ref, watch, reactive } from "vue";

let person = reactive({
  name: "张三",
  age: 18,
});

function changeName() {
  person.name += "~";
}

function changeAge() {
  person.age++;
}

function changePerson() {
  Object.assign(person, {
    name: "王五",
    age: 24,
  });
}

watch(person, (newValue, oldValue) => {
  console.log("person对象修改", newValue, oldValue);
});
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
