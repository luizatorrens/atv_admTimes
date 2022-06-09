<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      times: [
        {
          id: "f12bc7ce-5ca7-4cbf-ac6e-be3e59cb2862",
          time: "time 1",
        },
        {
          id: "b880659d-5d33-4607-ae19-8a22a738b509",
          time: "time 2",
        },
        {
          id: "0f97fea6-72ac-4ee0-bf1b-92516d3417e1",
          time: "time 3",
        },
        {
          id: "25c441be-e90a-4847-98a7-0d888e4c981f",
          time: "time 4",
        },
      ],
      jogadores: [
        {
          id: "ac803529-5e2d-45b2-a907-ca993bb301ea",
          nome: "jogador 1",
        },
        {
          id: "610e1ad0-0302-492e-a686-9bfb62cc2a82",
          nome: "jogador 2",
        },
        {
          id: "29eaba8d-a376-485e-9509-5dddd6587f0d",
          nome: "jogador 3",
        },
        {
          id: "d7c068f0-928f-4858-9ae3-eadc32edb230",
          nome: "jogador 4",
        },
      ]
    };
  },
  methods: {
    salvar() {
      const novo_id = uuid();
      this.times.push({
        id: novo_id,
        name: this.novo_time,
      });
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerencimento de Jogadores</h2>
    </div>
    <div class="form-input">
      <input type="text" v_model="novo_nome" placeholder="Nomes" />
      <input type="text" v_model="novo_time" placeholder="Times" />
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
            <td>???</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style></style>
