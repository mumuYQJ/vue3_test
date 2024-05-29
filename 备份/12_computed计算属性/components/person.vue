<template>
  <div>
    姓：<input type="text" v-model="firstName" /><br />
    名: <input type="text" v-model="lastName" /><br />
    <button @click="updateName">修改姓名</button><br />
    <button @click="fullChange()">修改全名</button>
    <p>全名：{{ fullName }}</p>
  </div>
</template>

<script lang="ts" setup name="person234">
import { computed, ref } from "vue";

let firstName = ref("张");
let lastName = ref("三");

function updateName() {
  firstName.value = "李";
  lastName.value = "四";
}

function fullChange() {
  fullName.value = "王-武";
}

let fullName = computed({
  get() {
    return (
      firstName.value.slice(0, 1).toUpperCase() +
      firstName.value.slice(1) +
      "-" +
      lastName.value
    );
  },
  set(val) {
    let names = val.split("-");
    firstName.value = names[0];
    lastName.value = names[1];
  },
});
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
