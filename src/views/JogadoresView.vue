<script>
export default {
  data() {
    return {
      jogadores: [
        { id: 1, name: "Jogadoor 1" },
        { id: 2, name: "Jogador 2" },
        { id: 3, name: "Jogador 3" },
        { id: 4, name: "Time 4" },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerencimento de Jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" />
      <button>Salvar</button>
    </div>
    <div class="list-items">
      <table>
        <thead>
          <tr>
            <td>ID</td>
            <td>Nomes</td>
            <td>Time ID</td>
            <td>Ações</td>
          </tr>
        </thead>
        <tbody>
          <tr v-for="jogador in jogadores" :key="jogador.id">
            <td>{{ jogador.id }}</td>
            <td>{{ jogador.name }}</td>
            <td>???</td>
            <td>Time 1</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style></style>
