<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <oldTab :valeur="fullName"/>
    <div v-if="isLoading">loading...</div>
    <newTab v-else :newValeur="newFullName"/>
  </div>
</template>

<script>
import oldTab from './components/oldTab.vue';
import newTab from './components/newTab.vue';


export default {
  name: 'App',
  components: {
    oldTab,
    newTab
  },
  data(){
    return{
      nom: "anarana",
      prenom: "fanampiny",
      nouveauNom:"name",
      isLoading:true,
    };
  },

  methods:{
    async changeValue(){
      await setTimeout(() => {
        this.nom = "bob";
        this.nouveauNom="newname",
        this.isLoading = false;
      }, 3000);
    }
  },

  computed:{
    fullName(){
      return this.nom + " " + this.prenom;
    },

    newFullName(){
        return this.nouveauNom + " " + this.prenom;
    }
  },

  watch:{
    nom:{
      handler(){
        console.log("watch after change this.nom :>> ", this.nom);
      }
    }
  },

   created() {
    this.changeValue();
  },
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
