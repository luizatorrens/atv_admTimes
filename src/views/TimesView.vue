<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      times: [
        { id: "f12bc7ce-5ca7-4cbf-ac6e-be3e59cb2862", name: "Time 1" },
        { id: "b880659d-5d33-4607-ae19-8a22a738b509", name: "Time 2" },
        { id: "0f97fea6-72ac-4ee0-bf1b-92516d3417e1", name: "Time 3" },
        { id: "25c441be-e90a-4847-98a7-0d888e4c981f", name: "Time 4" },
      ],
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
      <h2>Gerencimento de Times</h2>
    </div>
    <div class="form-input">
      <input type="text" v-model="novo_time" placeholder="Times" />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-items">
      <table>
        <thead>
          <tr>
            <td>ID</td>
            <td>Nomes</td>
            <td>Ações</td>
          </tr>
        </thead>
        <tbody>
          <tr v-for="time in times" :key="time.id">
            <td>{{ time.id }}</td>
            <td>{{ time.name }}</td>
            <td>???</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style></style>
