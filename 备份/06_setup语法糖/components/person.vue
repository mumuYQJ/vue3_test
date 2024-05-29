<template>
  <div>
    <p>{{ name }}</p>
    <p>{{ age }}</p>
    <p>{{ sex }}</p>
    <button @click="showAge">查看年龄</button>
    <button @click="showSex">查看性别</button>
  </div>
</template>

<script lang="ts" setup name="person234">
let name = "王五";
let age = 18;
let sex = "女";

function showAge() {
  age++;
  alert(age);
}

function showSex() {
  alert(sex);
}
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
