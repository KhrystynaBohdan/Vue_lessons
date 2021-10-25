<template>
  <h1> {{ title }}</h1>
  <p>Welcome...</p>
  <teleport to=".modals" v-if="showModal">
    <Modal theme="sale" v-on:click="toggleModal">
      <slot>
        <template>
          <a href="#">sign up now</a>
          <a href="#">more info</a>
        </template>
        <h1>welcome</h1>
        <p>coco</p>
      </slot>
    </Modal>
  </teleport>
  <teleport to=".modals" v-if="showModalTwo">
    <Modal v-on:click="toggleModalTwo">
      <slot>
        <h1>welcome2</h1>
        <p>coco2</p>
      </slot>
    </Modal>
  </teleport>
  <button v-on:click.alt="toggleModal">open modal(alt)</button>
  <button v-on:click.shift="toggleModalTwo">different modal</button>
</template>

<script>
import Modal from "./components/Modal";

export default {
  name: "App",
  components: { Modal },
  data() {
    return {
      showModalTwo: false,
      showModal: false
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo;
    }
  }
};
</script>

<style>
#app, .modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  color: red;
}

</style>
