<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      jogadores: [
        {
          id: "ac803529-5e2d-45b2-a907-ca993bb301ea",
          nome: "jogador 1",
          time: "Time 1",
        },
        {
          id: "610e1ad0-0302-492e-a686-9bfb62cc2a82",
          nome: "jogador 2",
          time: "Time 2",
        },
        {
          id: "29eaba8d-a376-485e-9509-5dddd6587f0d",
          nome: "jogador 3",
          time: "Time 3",
        },
        {
          id: "d7c068f0-928f-4858-9ae3-eadc32edb230",
          nome: "jogador 4",
          time: "Time 4",
        },
      ],
    };
  },
  methods: {
    salvar() {
      if (this.novo_jogador !== "") {
        const novo_id = uuid();
        this.jogadores.push({
          id: novo_id,
          name: this.novo_jogador,
        });
        this.novo_jogador = "";
      }
    },
    excluir(time) {
      const indice = this.times.indexOf(time);
      this.times.splice(indice, 1);
    },
  },
  salvar() {
    if (this.novo_time !== "") {
      const novo_id = uuid();
      this.times.push({
        id: novo_id,
        name: this.novo_time,
      });
      this.novo_time = "";
    }
  },
  excluir(time) {
    const indice = this.times.indexOf(time);
    this.times.splice(indice, 1);
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerencimento de Jogadores</h2>
    </div>
    <div class="form-input">
      <input
        type="text"
        v-model="novo_time"
        @keyup.enter="salvar"
        placeholder="Times"
      />
      <input
        type="text"
        v-model="novo_jogador"
        @keyup.enter="salvar"
        placeholder="Jogadores"
      />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-items">
      <table>
        <thead>
          <tr>
            <td>ID</td>
            <td>Nomes</td>
            <td>Time</td>
            <td>Ações</td>
          </tr>
        </thead>
        <tbody>
          <tr v-for="jogador in jogadores" :key="jogador.id">
            <td>{{ jogador.id }}</td>
            <td>{{ jogador.name }}</td>
            <td>{{ jogador.time }}</td>
            <td>
              <button>Editar</button>
              <button @click="excluir(jogador)">Apagar</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style></style>
