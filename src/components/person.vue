<template>
  <div>
    <p>姓名：{{ person.name }}</p>
    <p>年龄：{{ person.age }}</p>
    <p>c1:{{ person.car.c1 }}</p>
    <p>c1:{{ person.car.c2 }}</p>
    <button @click="changeName">修改姓名</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="changePerson">修改对象</button>
    <button @click="changeC1">修改c1</button>
    <button @click="changeC2">修改c2</button>
    <button @click="changeCar">修改车</button>
  </div>
</template>

<script lang="ts" setup name="person">
import { ref, watch, reactive } from "vue";

let person = reactive({
  name: "张三",
  age: 18,
  car: {
    c1: "奥迪",
    c2: "保时捷",
  },
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
