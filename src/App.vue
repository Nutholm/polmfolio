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
  name: "App",

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
@import url("https://fonts.googleapis.com/css2?family=Quicksand&display=swap");
@import url('https://fonts.googleapis.com/css2?family=Goblin+One&display=swap');
#app {
  font-family: "Quicksand", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: linear-gradient(
    map-get($Colorscheme, Quaternary) 10%,
    map-get($Colorscheme, Quaternary) 12%,
    map-get($Colorscheme, Primary),
    map-get($Colorscheme, Secondary),
    map-get($Colorscheme, Tertiary)
  );
}
</style>
