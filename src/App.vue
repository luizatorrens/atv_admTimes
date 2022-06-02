<script setup>
import HeaderComp from "./components/template/HeaderComp.vue";
import RodapeComp from "./components/template/RodapeComp.vue";
</script>
<template>
  <HeaderComp />
  <RouterView />
  <RodapeComp />
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  /*padding: 2rem;*/
  height: 100vh;

  font-weight: normal;
}
header {
  background-color: lightcoral;
  color: white;
  height: 5%;
  font-size: 1.3rem;
  display: flex;
}
footer {
  background-color: lightblue;
  color: rgb(29, 29, 173);
  height: 5%;
  font-size: 1.3rem;
}
main {
  height: 90%;
  background-color: rgb(228, 186, 186);
  color: black;
}
a {
  text-decoration: none;
  color: inherit;
}
</style>
