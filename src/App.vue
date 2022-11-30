<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('Zelda')">Change name</button>
    <button @click="changeAge('30')">Change name</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

type Age = number | string;

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: "Link",
      age: 25 as Age,
    };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
    changeAge(age: Age) {
      this.age = age;
    },
  },
});
</script>

<style></style>
