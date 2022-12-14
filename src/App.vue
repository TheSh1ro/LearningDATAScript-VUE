<script setup>
import { RouterView } from "vue-router";
import PageHeader from "./components/PageHeader.vue";
</script>

<template>
  <PageHeader id="header" />
  <RouterView id="main" />
</template>

<style>
* {
  margin: 0px;
  padding: 0px;
  list-style-type: none;
  text-decoration: inherit;
  color: inherit;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}
#app {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 8vh 1fr;
}
#main {
  min-height: 92vh;
}
</style>
