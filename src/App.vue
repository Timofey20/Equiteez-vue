<template id="app">
  <Header />
  <main>
    <Equity />
    <Securities />
    <Quote />
    <Products />
  </main>
</template>

<script>
import Header from "./components/Header";
import Equity from "./components/Equity";
import Securities from "./components/Securities";
import Quote from "./components/Quote";
import Products from "./components/Products";

export default {
  name: "App",
  components: {
    Header,
    Equity,
    Securities,
    Quote,
    Products,
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body {
  font-family: "Open Sans", sans-serif;
  overflow-x: hidden;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
