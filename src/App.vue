<template>
  
  <v-app>
    <div id="app">
    <myHeader id="myHeader"></myHeader>
    <myContent id="myContent"></myContent>
    <myFooter id="myFooter"></myFooter>
  </div>
  </v-app>

  
  
  
</template>

<script>
import Header from "./components/Header";
import Content from "./components/Content";
import Footer from "./components/Footer";

export default {
  name: 'App',

  data: () => ({
    //
  }),
   components: {
    myHeader: Header,
    myContent: Content,
    myFooter: Footer,
  },
};
</script>


<style lang="scss">
@import "./src/styles/variables.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // background-color: map-get($Colorscheme, Primary);
  color: black
}

</style>
