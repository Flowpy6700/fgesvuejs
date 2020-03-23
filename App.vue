<template>
  <div id="app">
    <Title :title="title"/>
    <Owner :owner="owner" :ownerSeen="ownerSeen" :buttonText="buttonText" :displayOwner="displayOwner"/>
    <Colors :colors="colors"/>
    <Calculatrice :calculatrice="calculatrice"/>
    <Filtre :filtre="filtre"/>
    <MetersForm :meters="meters"/>
    <Carrousel :carroussel="carroussel"/>
    <Liste :liste="liste"/>
  </div>
</template>

<script>
import Title from './components/Title.vue'
import Owner from './components/Owner.vue'
import Colors from './components/Colors.vue'
import Calculatrice from './components/Calculatrice.vue'
import Filtre from './components/Filtre.vue'
import MetersForm from './components/MetersForm.vue'
import Carrousel from './components/Carrousel.vue'
import Liste from './components/Liste.vue'

export default {
  name: 'App',
  components: {
    Title, 
    Owner, 
    Colors,
    Calculatrice,
    Filtre,
    MetersForm,
    Carrousel,
    Liste
  }, 
  data: () => {
    return {
      title: "Exercice 1", 
      owner: "Florian", 
      ownerSeen: false, 
      buttonText: "Afficher le propriétaire",
      colors: [
        { id: 1, name: "red" },
        { id: 2, name: "green" },
        { id: 3, name: "blue" }
      ]
    }
  },
  methods: {
    displayOwner() {
      this.ownerSeen = !this.ownerSeen;
      (this.ownerSeen) ? (this.buttonText = "Masquer le propriétaire") : (this.buttonText = "Afficher le propriétaire");
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
