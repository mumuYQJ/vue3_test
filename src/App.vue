<template>
  <div>
    <person />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import person from "./components/person.vue";

export default defineComponent({
  name: "App",
  data() {
    return {
      message: "Hello,World!Hello,Spring",
    };
  },
  components: { person },
});
</script>

<style>
p {
  color: blue;
  text-decoration: dashed;
  font-size: 24px;
}
</style>
