<template>
  <div id="app">
      <input v-model="firstValue" type="text">
      <input v-model="operator" type="text">
      <input v-model="secondValue" type="text">
    <p>
        Le resultat est : {{ resultat }}
        <button v-on:click="calculate">Calculer</button>
    </p>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data: () => {
      return {
          valeur1: 3,
          valeur2: 5,
          resultat: 0
      }
  },
  methods: {
      calculate() {
          this.resultat = parseInt(this.firstValue) + parseInt(this.secondValue)
      }
  }
}
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
</style>