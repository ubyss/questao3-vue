<template>
  <Main :cor="cor" :valor="valor">
    <template v-slot:default>
      <div class="container">
        <label>
          Digite seu texto
          <input type="text" name="" id="" v-model="texto" />
        </label>
        <label
          >Digite sua cor
          <input type="text" required v-model="cor" />
        </label>
        <label>
          Digite o tamanho
          <input type="number" required v-model="valor" />
        </label>
      </div>
    </template>

    <template v-slot:text>
      {{ texto }}
    </template>
  </Main>
</template>

<script>
import Main from "./components/Main.vue";
export default {
  name: "App",
  components: {
    Main: Main,
  },
  data() {
    return {
      cor: "DD9022",
      valor: "40",
      texto: "Texto padrão",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  display: flex;
  flex-direction: column;
  gap: 15px 0;
}
</style>
