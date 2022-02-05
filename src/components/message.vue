<template>
  <div class="content">
    <textarea
      class="text"
      v-model="text"
      name="comentarios"
      rows="10"
      cols="40"
    >
Escribe aquí tu mensaje</textarea
    >
    <br />
    <button v-on:click="enviar(text)">Enviar</button>
    <div class="mensajes">
      <div class="data" v-for="data in result" :key="data.id">
        {{ data.message }}
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data: () => ({
    result: null,
    text: null,
  }),
  async created() {
    let response = await axios.post("http://localhost:3000/write");
    this.result = response.data;
  },
  methods: {
    async enviar(data) {
      if (data != null) {
        let response = await axios.post("http://localhost:3000/write", {
          message: data,
        });
        this.result = response.data;
      }
    },
  },
};
</script>

<style scoped>
.mensajes {
  margin-top: 50px;
}
textarea.text {
  margin-top: 50px;
}
</style>