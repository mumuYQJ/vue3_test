<template>
  <div>
    <p>{{ message }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  data() {
    return {
      message: "Hello,World!Hello,Spring",
    };
  },
});
</script>

<style>
p {
  color: blue;
  text-decoration: dashed;
  font-size: 24px;
}
</style>
