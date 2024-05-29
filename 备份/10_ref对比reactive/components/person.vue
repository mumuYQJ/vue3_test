<template>
  <div>
    <p>一辆{{ cat.name }}车，价值{{ cat.price }}</p>
    <button @click="addPrice">增加价格</button>
    <button @click="changeCat">变更车的信息</button>
    <br />
  </div>
</template>

<script lang="ts" setup name="person234">
import { ref, reactive } from "vue";

//let cat = reactive({ name: "宝马", price: 100 });
let cat = ref({ name: "宝马", price: 100 });

function changeCat() {
  //Object.assign(cat, { name: "别克", price: 20 });

  cat.value = { name: "比亚迪", price: 30 };
}

function addPrice() {
  //cat.price += 10;
  cat.value.price += 10;
}
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
