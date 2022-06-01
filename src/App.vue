<template>
  <header>
    <span> Home </span>
    <span>|</span>
    <span> Times </span>
    <span>|</span>
    <span>Jogadores</span>
  </header>
  <main>Bem vindo!</main>
  <footer>OI LARI</footer>
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
  height: 15%;
  font-size: 1.3rem;
}
footer {
  background-color: lightblue;
  color: rgb(219, 59, 219);
  height: 15%;
  font-size: 1.3rem;
}
main {
  height: 70%;
  background-color: white;
  color: crimson;
}
header span {
  padding: 0 20px;
}
</style>
