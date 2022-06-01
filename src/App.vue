<template>
  <header class="menu-superior">
    <div class="menu-esquerdo">
      <span> Home </span>
      <span>|</span>
      <span> Times </span>
      <span>|</span>
      <span>Jogadores</span>
    </div>
    <div class="menu-direito">
      <span>Sair</span>
    </div>
  </header>
  <RouterView />
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
header span {
  padding: 0 20px;
}
header.menu-superior {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
