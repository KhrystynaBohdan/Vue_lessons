<template>
  <h1> {{ title }}</h1>
  <Modal :header="header" :text="text" theme="sale"/>
</template>

<script>
import Modal from "./components/Modal";
export default {
  name: "App",
  components: { Modal },
  data () {
    return{
      title: 'my first vue app',
      header: "hello cococ",
      text: 'forest club',
    }
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
h1{
  color: red;
}

</style>
