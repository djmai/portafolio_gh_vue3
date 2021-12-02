<template>
  <div>
    <Header title="Portafolio GH" />
    <Container />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Container from "./components/Container.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Container,
  },
};
</script>

<style>
* {
  font-family: "Roboto", Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
  margin: 0;
  padding: 0;
}
</style>
