<template>
  <div>
    <p>一辆{{ cat.name }}车，价值{{ cat.price }}</p>
    <button @click="addPrice">增加价格</button>
    <br />
    <ul>
      <li v-for="game in games" :key="game.id">{{ game.name }}</li>
    </ul>
  </div>
</template>

<script lang="ts" setup name="person234">
import { reactive } from "vue";

let cat = reactive({ name: "宝马", price: 100 });
let games = reactive([
  { id: "addf1", name: "王者荣耀" },
  { id: "addf2", name: "原神" },
  { id: "addf3", name: "明日方舟" },
  { id: "addf4", name: "守望先锋" },
]);

function addPrice() {
  cat.price += 10;
}
</script>

<style scoped>
div {
  background-color: aquamarine;
  padding: 10px;
}
</style>
